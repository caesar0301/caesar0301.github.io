---
title: R packages you should put under your pillow
date: 2015-05-20
comments: true
categories: Tutorials
tags:
    - R
---


R在统计分析、机器学习、以及绘图上有着丰富的功能，基础安装包里的函数能够满足基本的需求，如果需要更多样化、复杂的数据处理，可以试着使用以下工具:

<!-- more -->

## 数据清洗转换 (Data wangling)

* DescTools (Tools for describing data and descriptive statistics)
* dplyr (面向data.frame，plyr的下次迭代，让R具有流式数据处理的风格）
* plyr (有用的ddply函数，参考http://www.r-bloggers.com/a-fast-intro-to-plyr-for-r/）
* reshape (数据变形的基本操作，丰富但底层)
* reshape2 (功能强大的melt和cast数据融合函数，reshape简版)
* tidyr (功能简单实用的长宽数据变化，reshape2简版)


## 绘图及颜色 (Colors and plots)

* colorRamps (多种颜色梯度生成，如matlab风格的颜色)
* Colors in ggplot2 (http://bit.do/SDnT)
* colorspace (Carries out mapping between assorted color spaces including RGB, HSV, HLS, CIEXYZ, CIELUV, HCL.)
* dichromat (Focused on palettes for color-impaired viewers. Collapse red-green or green-blue distinctions to simulate the effects of different types of color-blindness.)
* ggplot2 (小清新绘图，事实上比基础绘图函数强大很多)
* ggvis (交互式数据可视化)
* gplots (一些加强版数据可视化函数，如boxplot2)
* grDevices (The base colors in core R, including well-known functions like colors, palette.)
* gridExtra (帮助ggplot2实现窗格布局，类似于基础包里的layout,mfrow函数)
* IDPmisc (Contains different high-level graphics functions for displaying large datasets)
* plotrix (多种不常见但可能有用的图形)
* RColorBrewer (The packages provides palettes for drawing nice maps shaded according to a variable)
* rgl (支持3D图形、视频生成，包括多种格式)
* scatterplot3d (绘制3D的散点图或平面)


## 模型和机器学习 (Machine learning)

* caret (The “go to” package for machine learning, classification and regression training)
* depmixS4 (Hidden Markov Model及其他dependent mixture model实现)
* e1071 (Good svm implementation and other machine learning algorithms)
* entropy (多种计算序列熵的方法)
* partykit (Tools for plotting decision trees)
* pracma (Functions for numerical analysis, linear algebra, optimization, differential equations and some special functions)
* psych (源自心理学研究人员，table和相关分析等)
* survMisc (Relatively new package with various functions for survival data extending the methods available in the survival package.)


## 随机分布参数估计 (Parameters estimation)

* fBasics (包含skewness和kurtosis函数)
* fitdistrplus (对MASS包参数估计函数的加强，同时有灵活的QQ图以及分布对比图)
* fitting{brainwaver}
* Goodness-of-test: goodfit{vcd}, chisq.test, ks.test, qqnorm
* MASS (最大似然估计fitdistr函数)
* mixdist (混合模型的参数估计)
* mixtools (混合模型的参数估计，CRAN Cluster View更多关于mixture model 的信息)
* Normality test: shapiro.test, jarque.bera.test{tseries}, sf.test{nortest}, ad.test{nortest}, cvm.test{nortest}, lillie.test{nortest}, pearson.test{nortest}
* poweRlaw (重尾分布参数估计)
* 参数估计函数：optim{stats}, mle{stats4}, fitdistr{MASS}


## Misc工具箱 (Misc tookit)

* classInt (包含离散化函数，如绘图中颜色的分阶)
* devtools (R包开发工具箱)
* Hmisc (functions for data analysis, graphics, utilities and much more)
* magicaxis (magplot, magaxis, maglab etc.)
* MASS (各种工具函数)
* misc3d (Misc 3d plots including isosurfaces)
* miscet (Miscellaneous R tools to simplify the working with data types and formats including functions for working with data frames and character strings)
* miscFuncs (Some functions for Kalman filters)
* pryr (深入理解R以及R包开发中的有用工具)
* scales (Scales map data to aesthetics.)
* sfsmisc (eaxis的对数坐标轴可实现类似magicaxis的效果)
* squash (Color-based visualization of multivariate data. Map numeric values to colors)
* stringr (Convenience wrappers for functions for manipulating strings)


## 优化工具 (Speedup)

* parallel (提供mclapply对lapply()和mapply()实现并行化处理。)
* doParallel (The "parallel backend" for `foreach` package. Must be enabled to use `%dopar%`.)
* foreach (Using foreach without side effects also facilitates executing the loop in parallel.)
* iterators (Support for iterators, which allow a programmer to traverse through all the elements of a vector, list, or other collection of data.)


## 地图工具 (Map tools)

* deldir (Calculates the Delaunay triangulation and the Dirichlet or Voronoi tessellation (with respect to the entire plane) of a planar point set.)
* geosphere (functions to calculate great circle distance.)
* GISTools (Some mapping and spatial data manipulation tools)
* mapmisc (New package with utilities for producing maps)
* mapproj (Mapping between lon/lat coordinates and projected surface.)
* maps (Display of maps. Projection code and larger maps are in separate packages (mapproj and mapdata)).
* maptools (Set of tools for manipulating and reading geographic data)
* NCmisc (A grab bag of utilities including progress bars and function timers)
* OpenStreetMap (Interfaces to OSM.)
* osmar (Interfaces to OSM.)
* splancs (Spatial Point-Pattern Analysis code in Splus.)


## 时空数据分析包 (Spatiotemporal)

* CompRandFld - Collect a set of procedures for the analysis of Random Fields by Composite Likelihood methods.
* fields (Fields is for curve, surface and function fitting with an emphasis on splines, spatial data and spatial statistics.)
* geoR (Geostatistical analysis including traditional, likelihood-based and Bayesian methods.Geostatistical analysis including traditional, likelihood-based and Bayesian methods.)
* gstat (Variogram modelling; simple, ordinary and universal point or block (co)kriging, sequential Gaussian or indicator (co)simulation; variogram and variogram map plotting utility functions.)
* PBSmapping (Facilitate the compilation and analysis of fishery data, particularly data referenced by spatial coordinates.)
* RandomFields (Simulation of Gaussian and extreme value random fields; conditional simulation; kriging; maximum likelihood estimation.)
* raster (Reading, writing, manipulating, analyzing and modeling of gridded spatial data.)
* rgdal (Provides bindings to GDAL)
* sp (Basic spatial and temporal classes and useful functions like spplot, Trellis plot, spDists, spsample.)
* spacetime (Classes and methods for spatio-temporal data, including space-time regular lattices, sparse lattices, irregular data, and trajectories)
* spdep (Spatial Dependence: Weighting Schemes, Statistics and Models)
* xts (Uniform handling of R's different time-based data classes by extending zoo)
* zoo (For Regular and Irregular Time Serie)


## 空间相关性 (Spatial correlation)

* ade4 - This package has function gearymoran that calculates Moran's I and Geary's c. Does not plot correlograms.
* ape - Moran's I test (function Moran.I) for spatial and phylogenetic autocorrelation (based on normal approximation, not on randomizations = fast). Does not plot correlograms.
* geosphere - a bunch of spherical trigonometry functions for geographic applications.
* mpmcorrelogram - I include it as a curiosity. It calculates Multivariate Mantel Correlograms.
* ncf - Provides functions correlog and spline.correlog. Plots correlograms. Does randomization tests.
* pgirmess - Has function correlog that calculates the correlogram. It uses normal approximation to test significance.
* raster - Simple function Moran. Works on rasters. You need to specify a simple neighborhood matrix. Does not plot correlograms.
* spatial - If I understand it correctly, this package first needs you to fit a trend surface (by kriging) and you can then calculate correlogram of this fitted surface. I haven't gone deeper into it.
* spdep - sp.correlogram, moran, moran.plot, moran.test, moran.mc. This is the most comprehensive package, and also the most difficult to work with. Does everything, has steep learning curve.

* 参考: http://www.r-bloggers.com/spatial-correlograms-in-r-a-mini-overview/


## 其他资源 (Public domains)

* R-bloggers: http://www.r-bloggers.com/
* Quick R: http://www.statmethods.net/
* CRAN Task View: http://cran.r-project.org/web/views/
* Advanced R: http://adv-r.had.co.nz/
* Quick list of useful R packages: http://bit.do/2cB6
* 让R成为你的GIS仓库: http://bit.ly/1twJPvI
* 统计中的样本检验基础和R实践: http://bit.ly/1Dy5uFZ
* 多源包搜索引擎: http://www.rdocumentation.org/

