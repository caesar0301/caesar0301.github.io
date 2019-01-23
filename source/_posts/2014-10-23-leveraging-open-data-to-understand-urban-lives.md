---
title: Leveraging open data to understand urban lives
date: 2014-10-23 12:00:00
tags:
    - GIS
    - OpenData
photos:
    - http://7xlgp4.com1.z0.glb.clouddn.com/blog-post08-nyc-taxi-one-day.png
---


Data mining, one of the hottest topics on the media in past years, exhibits a new way to help companies, organizations, and even ordinary people to make plans and decisions in near future. We are convinced by the knowledge derived from data, mostly because the data recording historical events is more solid and reliable than people's experience that is influenced by so many random factors in reality. In this post, I discuss the possibility to derive reliable ideas about urban human lives using open data (which is public and free to be available on Internet or other resources), and show some interesting open datasets to support our understandings.

<!-- more -->

## Freedom of information

Knowing how people in urban areas behave everyday is a promising way to understand the evolution of our social relationships, economic phenomena, public security, and important topics on saving energy and reducing environment pollutions to better our world. But finishing these tasks usually requires large-scale datasets to observe general rules and derive unbiased conclusions from a large population. As for the potential value of these data, its mostly controlled in the hand of governments and a small group of private cooperations.  The tragedy of [Aaron Swartz](http://en.wikipedia.org/wiki/Aaron_Swartz) also alerts us about the hardness towards free information share between people.

Concerns at the list top usually come from public (national) security, business secrets and personal privacy. I admit the importance of these aspects in our lives. But a parallel important fact is that we people own the freedom to share most information, and use these information to better our lives. A happier median solution may come from the development of anonymization techniques and control mechanisms of information access, yet not the completely cut-off of information air.


## Large-scale urban data

Despite the previous concerns, there have occurred some interesting data that records citizen behaviors and is public to support extensive studies and analyses. Public transportation systems are one of the existing sources. The access of these information facilitates efficient management of transportations resources and brings about convenience for users. Other sources include the 311 calls and taxi cab trips in New York city, as well as one mobile network traffic dataset in my previous researches.


### Bike Share Systems (BSS)

[![Bicycle sharing system](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post08-hangzhou_bike_sharing_station.jpg)](http://en.wikipedia.org/wiki/Bicycle_sharing_system)

Recent years, many large cities over the world have their [bicycle sharing system](http://en.wikipedia.org/wiki/Bicycle_sharing_system) to lower the pressure of transportation systems and reduce the discharge of green house gas. A happy news is that most of these BSS runners have opened their data to stimulate new applications and optimize the management of their resources. Known applications contains the clustering of customer usage patterns and the prediction of available bikes in each stock. By connecting available resources in physical world and personal preferences, future applications can be the development of intelligent tour guides, and some social activities on the bike-riding networks.

[Nice Ride](https://www.niceridemn.org/) is a company in Minnesota, US, running a bike sharing networks in the urban area. This company is one of the pioneers to make the data available. The first public version of 2011 gives the initial station network and trip histories with subscriber info (ID, date of birth, gender, ZIP code). Each individual trip with start and stop info is recorded. The [following years](https://github.com/MinnPost/minnpost-nice- ride) removed the subscriber data to protect privacy at the request of [Anton Schieffer](http://antonschieffer.com/2012/12/nice-ride-and-user-privacy-crossing-the-line/). A nice visualization of these data is given by Alan Palazzolo et al. on MinnPost, [A day in the life of Nice Ride bikes](http://www.minnpost.com/data/2012/06/day-life-nice-ride-bikes).

[Hubway](http://www.thehubway.com/) in MA and [CitiBike](http://www.citibikenyc.com/) in New York City, US also publish similar trip history, yet without subscriber ID (only subscriber type, ZIP code, birth of date, and gender). Theoretically, subscriber profile still can be restored from these demographic information at higher accuracy. We can develop identification algorithm and evaluate with the Nice Ride 2011 dataset. The trip history (since July, 2013) and live station feeds of CitiBike are able to be fetched from [CitiBike data site](http://www.citibikenyc.com/system-data) . The static data of Hubway (since July, 2011) can be obtained from [Hubway data visualization challenge](http://hubwaydatachallenge.org/).

The other two companies come from Washington DC, US ([CapitalBikeshare](http://www.capitalbikeshare.com)) and London, UK ([Barclays Cycle Hire](http://www.tfl.gov.uk/modes/cycling/barclays-cycle-hire)). These two datasets almost remove the subscriber info thoroughly and only trip history is available. The CapitalBikeshare publishes the data since the forth quarter of 2010 and Barclays since 2012. Both contribute millions of bike journeys in the cities.

**Applications**: Before use these data, we must imagine that these data records both spatial and temporal points of a trip. Without subscriber information, we can not trace an individual, but the transportation demands of a portion of citizens are present. The next step is depending your imaginations.


### New York 311 calls

311 is New York City's main source of government information and non-emergency services. The first use of 3-1-1 for informational services was in Baltimore, Maryland, where the service commenced on 2 October 1996. 3-1-1 is intended to connect callers to a call center that can be the same as the 9-1-1 call center, but with 3-1-1 calls assigned a secondary priority, answered only when no 9-1-1 calls are waiting. This system is intended to extend the system such that true emergency callers are answered quickly with highest priority. [311 service requests since 2010](https://nycopendata.socrata.com/d/erm2-nwe9) are availabe at [NYC OpenData site](https://nycopendata.socrata.com/). You can associate this repository with other datasets like transportation services.

[![NYC311](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post08-nyc311.jpg)](https://nycopendata.socrata.com/d/erm2-nwe9)


### New York Taxi Cab trip

This dataset contains the taxi trip in NY, 2013 and is first FOILed ((The Freedom of Information Law) by civic hacker and downtown Brooklyn resident Chris Whong. He discovered the [Taxi! video](http://vimeo.com/31298658) and ask the author if the data would be available. Surprisingly, the response states that [this data was FOILable](http://chriswhong.com/open-data/foil_nyc_taxi/). After publication of data, he also work out a stunning visualization of [NYC Taxis: A Day in the Life](http://nyctaxi.herokuapp.com/) (The back-end techniques are also described in his blogs, [part 1](http://chriswhong.com/data-visualization/taxitechblog1/) and [part 2](http://chriswhong.com/open-data/taxi-techblog-2-leaflet-d3-and-other-frontend-fun/)).

[![herokuapp](http://7xlgp4.com1.z0.glb.clouddn.com/blog-post08-nyc-taxi-one-day.png)](http://nyctaxi.herokuapp.com/)

- [Torrent for 2013 Trip Data (11.0GB)](http://chriswhong.com/wp-content/uploads/2014/06/nycTaxiTripData2013.torrent)
- [Torrent for 2013 Fare Data (7.7GB)](http://chriswhong.com/wp-content/uploads/2014/06/nycTaxiFareData2013.torrent)


### Mobile Network Traffic Data

Operational cellular network data is rare in research communities, especially with the topology of the observed networks. We [publish this dataset](https://github.com/caesar0301/MSTD) to fill this gap following the publish of our research paper "*Modeling and Analyzing Spatio-Temporal Dependence of Cellular Traffic at City Scale*".  For the analysis of cellular traffic dependence over space and time, we perform collections of this dataset in a developed city in East China. Basic dimensions in this dataset are the space, time, and traffic statistics (including bytes, packets). A complete week-long measurement is included covering the most area of the city. The minimum spatial resolution of traffic is the coverage area of individual cellular base station (around 200~500m), and the minimum temporal resolution is one hour.


## Enjoy Open Data

Open data communities are rapidly developing now. We can expecting more and more precious data will be available on the Internet in near future. With these multi-source datasets, we are facing challenges to develop efficient algorithms to analyze and model these data. Challenges take company with opportunities. In the world of [Linked data](http://en.wikipedia.org/wiki/Linked_data), all entities are connected by underlying logic or natural rules. We are marching towards this goal but primarily to uncover the common patterns in multiple data sources. We are observing our world via [data holography](http://en.wikipedia.org/wiki/Holography) where the objective nature principles are holograhpically recorded in multi-source digital bits. In this sense, data miners, are also world observers.
