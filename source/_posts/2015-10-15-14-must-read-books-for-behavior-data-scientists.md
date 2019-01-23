---
title: 14 Must-Read Books for Behavior Data Scientists
date: 2015-10-15
comments: true
tags:
    - Mobility
---


![must-have-banner](http://7xlgp4.com1.z0.glb.clouddn.com/must_have.png)

In my Ph.D career, human behavior (especially mobility) analysis from telecommunication data is my studying theme.  I learned a bunch of theories and techniques from other domains when they are of convenience to analyze human mobility.  As for the intrinsic complexity of human behavior and intersection of behavior science, tools you should have in package are usually not a hammer but a flexible toolkit.  Different problems prefer specific classes of methods to solve. When you change views of the same problem with other theories, novel inspections may appear.  Here I introduce a mostly-related book list that is beneficial when you are either a green hand or an expert in the domain.

<!-- more -->

## Statistics for Behavior Science

For a data scientist, statistics is primary in the toolkit. You use distribution to know the scale and variance of collected data. You also need hypothesis tests to check the significance of derived conclusions. Sometimes dataset is of small size as for high cost of data acquisition, sampling theory in statistics is essential to achieve a reliable result with limited observations.  Heiman made a basic theoretical package for these goals.

- Gary W. Heiman. *Basic Statistics for the Behavioral Sciences*, 7th ed. 2013.

If you are looking for a more practical explanation, McCall's work may deserve your attention.

- Robert B. McCall. *Fundamental Statistics for Behavioral Sciences*. 8th ed. 2000.


## Spatio-Temporal Data Analysis

One theoretical source of behavior science comes from physical statistics and thermodynamics, as a result of viewing mobile individuals as physical particles. A branch of concept and algorithms are introduced in this philosophy. With this individual-particle transformation, we get an opportunity to find more general and objective rules that govern human mobility. Cressie et al. made great contributions on this topic.  Two valuable books are preferred when I consider human behavior spatially or by coupling space and time.

- Cressie, N, and CK Wikle. *Statistics for Spatio-Temporal Data*. 2011.

- Cressie, Noel. *Statistics for Spatial Data*. Revised Edition edition. 1993.

If you are considering pure time series, I bet you will appreciate me with below:

- Brockwell, Peter J., and Richard A. Davis. *Introduction to Time Series and Forecasting*. 2nd edition. 2010.

As a R enthusiast, theories with efficient programmable possibility are my favorite.

- Metcalfe, Andrew V., and Paul S.P. Cowpertwait. *Introductory Time Series with R*. Springer New York, 2009.

- Use R!. *Applied Spatial Data Analysis with R*. Springer New York, 2008.


## Data Mining

Data mining is a wide concept, while it is narrow to replace data analysis with machine learning techniques these years.  Whatever, a behavior scientist should be open to learn efficient and advanced ideas that are proposed in ML domain. In my personal researches, I do not like the pure application of black-box ML models in my problems, except they provide better performance and reasonable insights into the problem. Several popular and high-quality DM/ML books are listed. If you are not familiar with machine learning concepts, Han et al. give a broad view:

- Han, Jiawei, and Micheline Kamber. *Data Mining Concepts and Techniques*. 2nd ed. 2006.

If you intend to dive into ML algorithms with deep theory, you may prefer

- Friedman, Jerome, Trevor Hastie, and Robert Tibshirani. *The Elements of Statistical Learning*. Vol. 1. 2001.

To learn the building blocks in ML algorithms and further absorb the spirit in your own models, Bishop's work may become a bible under your pillow.

- Bishop, Christopher M. *Pattern Recognition and Machine Learning*. New York: Springer, 2006.

For engineering practice using ML theory, you can check

- Witten, Ian H, and Eibe Frank. Data Mining: *Practical Machine Learning Tools and Techniques*. 2005.


## Complex Network

When we analyze human behavior in large scale or by coupling external factors, network theory is a powerful tool to address problems like social analysis and mobility pattern mining. On network theory with brief structure and beautiful illustration, I prefer the book of Albert-László, which is currently in ebook version,

- Albert-László, Barabási. *Network Science*. 2012. [Free on-line version](http://barabasi.com/networksciencebook/)

When we consider the flow dynamics over networks, flow theory is also essential.

- Ahuja, Ravindra K., Thomas L. Magnanti, and James B. Orlin. *Network Flows: Theory, Algorithms, and Applications*. 1st ed. 1993.


## Visualization

Last but not least, data visualization is also important when you present discoveries to others who are not familiar with your big problem. Clear and accurate figures convey much information than words. One basic principle for a beginner is that different data types have a small number of optimal visualization forms. Outstanding figures are mostly due to a choice of near-best presentation. From the `beautiful data`, I have learned basic design principles from many excellent works.

- Segaran, Toby, and Jeff Hammerbacher. *Beautiful Data: The Stories Behind Elegant Data Solutions*. 1st ed. 2009.
