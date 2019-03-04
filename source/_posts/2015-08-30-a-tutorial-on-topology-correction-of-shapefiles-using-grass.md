---
title: A tutorial on topology correction of shapefiles using GRASS
date: 2015-08-30
comments: true
tags:
    - GIS
    - Tools
---

**Abstract**: Here is some practical expeirience in cleansing the shapefile using [GRASS](https://grass.osgeo.org/), which is an open-source platform to do scientific analysis on spatial data.

[ERIS shapefile](https://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) is a popular format to store spatial vector data. Various geometrics (e.g. points, lines, polygons etc.) can be processed and exchanged in a compatibable way by different softwares. When I am doing a research to calculate the shortest paths between pairs of a set of points, one convenient method is converting the network topology stored in a shapefile into a [graph data structure](https://en.wikipedia.org/wiki/Graph_(abstract_data_type)) and performing spatial analysis with libraries like `igraph` or `graph` in R.

<!-- more -->

However, the shapefiles per se may have internal pitfalls after we obtained them from public domains. One of the common pitfalls in a shapefile is about the '[connectedness](http://www.esri.com/news/arcuser/0401/topo.html)' of line-shaped objects, including absent intersection of cross roads, dangling polylines and duplicated points etc. These pitfalls moslty lead to a large number of disconnected parts in a single road network and we can not perform the shortest-path algorithm directly on the topology. Thus we must conduct some connectivity correction on the raw shapefiles before our analyses in next stage.


## Obtain shapefile of target area

The geometric vector of target area is our ingrediant to go on this tutorial. [Bbbike.org](http://extract.bbbike.org/) is a great extracter for OpenStreetMap layers. You can select, extract and download any areas you want in any shapes by dragging the selective bounding box. For this post, I have prepared [a copy](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post15-SJTU.Minhang.OSM.shp.zip) of our university to continue following steps. There are eight layers including roads, waterways, railways, points, places, natural, landuse and buildings, which are the minimum data obtained from previous extractor.


## Install GRASS

On Mac OS X, you can install grass quickly with `brew`. This is recommended because the official version 7.0 dmg installer complains about the CPU arch under python 2.7 on my machine.

```shell
  $ brew search grass
  $ brew install grass-70
```


## Create new mapset (CLI mode)

Three components `<grassdb>/<location>/<mapset>` are to be understood to start from scratch:

- Default database: a default directory to store all GRASS data;
- GRASS location: this corresponds to your individual projects and you'd better keep separated projects in different locations;
- GRASS mapset: the actual working directory for yourself. Others' will be kept as distinctive mapsets in case that a team is sharing the same `PERMANENT` base but introducing different modification.

Create a new mapset in which `sjtu` is the location and `chenxm` indicates the mapset that is used by me. The GRASS promt is a modified CLI with built-in functionalities. Other commonds can be found on the [manual page](https://grass.osgeo.org/grass70/manuals/index.html).

```shell
  $ grass70 -c roads.shp ~/workspace/GRASS/sjtu -text
  $ > g.mapset -c chenxm
  $ > g.mapset chenxm
```

Import all shapefile layers into created mapset:

```shell
  $ > v.in.ogr input=../shape layer=roads --overwrite
```

## Correct topology connectivity

We use the `v.clean` toolkit to repair the topology pitfalls, in the sequence of

- `break` the cross and add intersection if it's absent
- `snap` undershot and overshot pologons
- `rmdangle` remove the dangling lines whose lenght is larger than a threshold
- `rmdup` remove the duplidated points

The threshold unit is **degree** when we are using the default coordination projection.

```shell
  $ > v.clean input=roads@chenxm output=roads_clean@chenxm type=point,line,area tool=break,snap,rmdangle,rmdupl thres=0.00,0.00003,0.00001,0.00 --overwrite
  $ > v.out.ogr input=roads_clean@chenxm output=roads_clean format=ESRI_Shapefile --overwrite
```

## Check out the performance

The topology correction removes the number of self-connected parts mostly by breaking the intersection and snapping the pitfalls. This accidently introduces over-correction as for the absence of information of real road networks, e.g. [great flyovers](https://www.google.com/search?q=giant+flyover). Nevertheless, this does not impact the result when we are involving the road network as suplementary analysis.

As show in figure below, the left is the original shapefile with 256 self- connected parts, and the middle figure gives the result after our correction with previous configurations. Actually, the resolution of topology is largely impacted by the selection of toolkit parameters. For example, we exhibit the snapping tool with threshold `0.0005` (right figure) which gives a rough sketch of underlying network. As for the personal requirements, you should experiment with multiple sets of parameters to get the satisfied result.


## Appendix:

```R
  #!/usr/bin/env R
  # file: check_conn.R
  # R script to check the connectivity of road network.
  library(shp2graph)
  rn<-readShapeLines("roads_clean/roads_clean.shp", proj4string=CRS(as.character(NA)))
  res<-nt.connect(rn) # the largest connected part
```

Run the script in terminal

```shell
  $ R --no-save]( check_conn.R
```
