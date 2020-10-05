---
layout: post
title: "LA County Thiessen Polygon Density Mappings: Narcotics, Grand Theft Auto, DUI, and Crimes Per Tract"
date: 2018-08-28
description: 
image: /assets/images/Crimes-Thiessen.png
author: Thomas Vaeth
tags: 
  - Thematic Mapping
---

### Intro:

To solve questions or ambiguities around proximity and predictive policing, this unit focuses on various methods such as density maps and heat maps. The first three heat maps illustrate 3 types of crime within Los Angeles County: Grand Theft Auto, Possession of Narcotics, and Driving Under the Influence. To find data for these crimes, I downloaded Part I and Part II data within the past month in Los Angeles County, courtesy of the Sheriff’s department. I imported this data (a CSV) into Arcmap as X,Y data to place the crime points on the map. The CA State Plane V layer was utilized to place the points in the correct manner. Lastly, the density tool in ArcToolbox was used to compute a kernel density .tif for each crime, and then overlaid on top of the unobtrusive light-grey canvas basemap. This process was done 3 times for each crime.

The last two maps were made palpable through a different method. These maps focus on predictive policing. Both maps contain the same crime data as the previous three (Grand Theft Auto, Possession of Narcotics, and Driving Under the Influence). A shapefile containing the amount of police stations/sheriff stations within Los Angeles County was then downloaded. Theissen polygons were produced (using the analysis proximity tool in ArcToolbox) around each police station; this allowed for an illustration of which zones were within closest proximity for the given police station’s response. I performed a spatial join with the crimes and the Thiessen polygons to assess the total amount of crimes within each polygon. This allowed for an analysis of which police station could use aided help/more resources to reduce crime. The polygons were color schemed by lowest to highest density of crimes. For the last map, the same overlay process was used—this time regarding Los Angeles Census Tracts, instead of Thiessen polygons around each station. The census tracts have a color scheme denoting which tracts have the highest concentration of crime, and ergo should require a larger concentration of officers patrolling.

Improvements could be made to make the legends more informative - like labeling htem 'low,'  'moderate,' 'high' etc.

### Los Angeles Criminal Mapping: Density Analysis of Reported Crimes

![Map GIS](/assets/images/Narcotics.png)

![Placeholder](/assets/images/GTA.png)

![Placeholder](/assets/images/DUI.png)

![Placeholder](/assets/images/Crime-per-tract.png)

![Placeholder](/assets/images/Crimes-Thiessen.png)
