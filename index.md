---
title       : Chicago Pothole Completion
subtitle    : 
author      : CBrown
job         : Johns Hopkins University - Data Products Course
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---



## Chicago, City of Open Data ... and Potholes

Chicago is a leading city in terms of open data practices.
https://data.cityofchicago.org/

It's only natural, given the reputation for clean and open government. Actually, that was a joke.

Chicago is more known for machine politics and 'clout'. If you know a guy that knows a guy, you can get something done. Like get a pothole in your neighborhood fixed.

Open data and clout politics seem like an unlikely mix, but hey, an open door is an open door. We thought it could be instructive to learn if open data would show relatively fair policies across the city, or if your likelihood of getting a pothole on your street fixed still depends greatly on the neighborhood you live in.

The title of the dataset used for this study is "311 Service Requests - Pot Holes Reported".



--- .class #id 



## About the Data


The data records contain multiple geographic divisions as follows (with count): Wards (50); Police Districts (26); Zip Codes (62); and Community Areas (77).

Wards might seem useful, as they are political divisions tied to an Alderman. But Wards are redistricted every 10 years and the boundaries have recently changed.

Police districts would be useful for crime statistics or 911 call data, but not 311.

Zip codes might be useful, but Chicagoans don't associate a location to most of the zip codes around the city, so it would be difficult for them to compare neighborhoods.

The Community Areas are really the best choice. The neighborhoods have been established for a long time. People identify with them, and Chicagoans generally have some idea of most of the neighborhoods on their 'side' of the city, and at least a few on the other side.
https://en.wikipedia.org/wiki/Community_areas_in_Chicago

The dataset was downloaded and cleaned of duplicates, records without a valid Community Area indicator, and a handful of outlier records of over 280 days to completion.


---

## Results

Each neighborhood is compared to the city average of 20.36 days and median of 7 days, with a 60-day completion chart displayed. Expected 60-day completion is in the mid-80% range.

If you know Chicago neighborhoods, you will probably find some surprises, and will definitely find some non-surprises.

Residents of the famously connected neighborhood of Bridgeport, ancestral home of the Daley clan, unsurprisingly (to a Chicagoan) can expect much faster repair times for their potholes. Their median repair time is 0 (zero) days, aka same day service. And their average time is 9.78, less than half of the city's 20.36 performance, with 95% completion within 60 days.

```r
9.78/20.36
```

```
## [1] 0.4804
```



---

## What's Next?


Mining other Chicago 311 service data (tree trimming, grafitti busting), to compare performance and gain a greater understanding of the how services are distributed across the city.

Tying 311 service data to US Census data to determine whether neighborhood characteristics like ethnicity, income, education level, family size, homeownership rates, etc. appear to have any relationship to service times.

Taking a closer look at the data to determine other factors that may legitimately impact response time. For example, integrating with vehicle traffic data to determine high traffic areas that could reasonably be expected to demand faster than normal pothole repair times because of greater visibility and impact.

Comparing reporting rates in different neighborhoods to try to gauge community involvement.

Incorporating maps to show neighborhood locations into the results pages.




