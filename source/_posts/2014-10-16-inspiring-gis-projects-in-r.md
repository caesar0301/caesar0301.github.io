---
title: Inspiring GIS projects in R
date: 2014-10-16 17:06:00
comments: true
tags:
    - GIS
    - R
photos:
    - http://7xlgp4.com1.z0.glb.clouddn.com/blog-post07-topography.png
---


[R](http://www.r-project.org/) is a free software for statistical computing and graphics (as declaimed in its project vision). But in my view, its horizon is beyond that thanking to its flexible extension infrastructure. As a PhD student leveraging data mining techniques in computer network measurement and analysis, I am even shocked by the community passion and creativity after an experienced (more or less) journey in R world.

R has facilitated my daily mining tasks as a tiny *Swiss-army-knife* in pocket, from data collection, wangling, and transforming, to modeling, visualization, and more importantly, communication with others. In this blog, I collect and make a list about some inspiring GIS ([Geographic Information System](http://en.wikipedia.org/wiki/Geographic_information_system>)) projects (mostly using R) that inspire me in my studies and provide me another vantage point to see this world *dataly*.

<!-- more -->

## Preliminaries

Through this journey, I do not require any programming experience from you in R, or even other computer languages. What you need to know is this is just a computer tool and you can also produce the following artistic works when you know how to use it. I bet more, you will fall in love with it. (You are safe to skip to next section if you have no plan to learn this tool for now.)

For readers who want to practice R, I also prepare a table of "quick-start" meal for you. These are actually the material from which I learn this language. Do not be frightened by the "steep learning curve" statement elsewhere. It is there only if you are trying to learn R from previous experience of other programming languages. **Leaning from scratch, that's my advice**.

- [R Official Site](http://www.r-project.org/): First you need to install R environment on your computer. Because R is cross-platform, you can [download](http://cran.rstudio.com/) and install corresponding binaries for your system.

- [RStudio](http://www.rstudio.com/): This may be the best option to edit, debug, or even publish your own packages and applications within an integrated IDE.

- [Quick-R](http://www.statmethods.net/): This may be your first arrival in real R's world. This site is created to help the user quickly access the power of R in their own work. More details in each part of this site can be read in the book [R in Action (2nd Edition)](http://www.manning.com/kabacoff2/).

- [CRAN Task View](http://cran.r-project.org/web/views/): You will like these repositories if you are an expert in specific domain and want to leverage R's packages in your researches. For example, the task view "Spatial" and "SpatioTemporal" would be preferred by GIS users or others interested in sptial and temporal series.

- [Advanced R](http://adv-r.had.co.nz/): A book (still in-progress when I write this blog) is written by Hadley Wickham for advanced users to learn or comprehend the core concepts in R and become a professional R developers.

- [R Bloggers](http://www.r-bloggers.com/): One of my heavily accessed website to keep up with the development of community. I have learned many modeling and visualization techniques since my first discovery of this site.

- [R Documentation](http://www.rdocumentation.org/): A documentation hub to search R packages from CRAN repositories, [bioconductor](http://www.bioconductor.org/), and [GitHub](http://www.github.com).


## Projects

I have make up serveral creteria to filter out other projects in face of what I want. The most important rule is that **the work is mainly generated with R language**. Due to the data scale, sometimes, the author requires other tools to manipulate the raw data and this does not affect our selection. The second rule is that the work must be inspiring for others (feel free to propose your ideas in comments), either impressive or useful in uncovering the data information. Okey, finally, it is about GIS, for this list.


### Using R as a GIS

This is a [tutorial](http://pakillo.github.io/R-GIS-tutorial/) contributed by [Francisco Rodriguez-Sanchez](http://sites.google.com/site/rodriguezsanchezf) to perform basic operations with spatial data in R, such as importing and exporting data (both vectorial and raster), plotting, analyzing and making maps. Also [github site](https://github.com/Pakillo/R-GIS-tutorial). Here is an example to plot Europe countries using the package **rworldmap**:

![worldmap](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post07-rworldmap.png)


### Mapping the world’s biggest airlines

This colored map [visualizes the top 7 airlines in the world](http://spatialanalysis.co.uk/2012/06/mapping-worlds-biggest-airlines/). It is totally generated with open data and R (i.e., a graphical package [ggplot2](http://ggplot2.org/). The author combines the urban area of [dense human habitation](http://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-urban-area/) and the airline [route data](http://sourceforge.net/p/openflights/code/HEAD/tree/openflights/data/routes.dat?format=raw) from [OpenFlights](http://openflights.org/data.html). The beautiful style inherits the spirit of "[Earth at Night](http://apod.nasa.gov/apod/ap001127.html)" which is a composite of hundreds of pictures made by the orbiting DMSP satellites.

![airlines](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post07-airlines.jpg)


### Visualising topography

[Robin Edwards](http://geotheory.co.uk/), a researcher at UCL CASA, has created these [stunning topographic](http://geotheory.co.uk/blog/2014/02/07/visualising-topography/) maps using the high resolution elevation data provided by the British Oceanographic Data Centre. The transitions from black (high areas) to blue (low areas) give the maps a slightly ethereal appearance to dramatic effect.

![topography](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post07-topography.png)


### Facebook friends network

You have possibly seen this figure in other media to illustrate the impacts of social networks on our lives. This figure is created by [Paul Butler](http://paulbutler.org/) when he was an intern in Facebook, 2010. The details are given [here](http://on.fb.me/1CucrEA) and [here, too](http://paulbutler.org/archives/visualizing-facebook-friends/). The main challenge is to adjust the plotting order and colors of lines regarding the line weight (number of friends).

![facebook-worldmap](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post07-facebook-network.jpg)
