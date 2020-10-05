---
layout: post
title: "Modifications of T-Mobile Cell Towers for Accentuated Coverage Areas: Los Angeles, CA"
date: 2017-08-30
description: 
image: /assets/images/t-mobile-cell-coverage.png
author: Thomas Vaeth
tags: 
  - Raster Analysis
---

### Intro:

This week’s assignment focused on advanced methods of raster analysis to calculate the coverage area of T-Mobile cell towers in Los Angeles County. The outline of the county was highlight vis-à-vis an array of downloaded GeoTIFF’s (digital elevation models) from USGS EarthExplorer. These were then coverted into rasters, through the “Mosaic to New Raster” option in ArcToolbox. The specific locations for each cell tower were achieved through a CSV, downloaded on T-Mobile’s website. This CSV was then converted into a shapefile, with its attribute table being edited to meet each required element—an increased range of 30000km (map 1), and increased tower height of 10m (map3), and 3 added tower locations for an overall increase in coverage (map 4). All in all, the assignment fringed upon the viewshed analysis tool, which allowed for these hypothetical adjustments to the cell towers to come to fruition.

Improvements could be made by using a different color scheme/representation to illustrate the improved (increased) range in coverage.

![Map GIS](/assets/images/t-mobile-cell-coverage.png)

Map 1 illustrates the current placement of T-Mobile towers in Los Angeles County. In total, there are 104 cell towers, the majority of which are concentrated in central and southern Los Angeles. The towers height, radius, and several factors about the earth’s trajectory were set at given increments. The total amount of area not covered in Los Angeles County came out to 58.9%, an average calculated by dividing the maximum (7,247,374,591.051,817) by the sum (12,301,062,346.864,695). To find the average area covered by current T-Mobile towers, this number was subtracted by 100. As is, 41.1% of LA County is covered by T-Mobile.

![Placeholder](/assets/images/3-added-towers.png)

Map 4 offers an insight to what adding an additional 3 cell towers to LA County would achieve for improving T-Mobile’s overall cell service. I chose 3 areas that were lacking in coverage: Malibu, Palmdale, and Lancaster. The same parameters for map 3 were held constant. Creating 3 new towers had the most significant result on increasing T-Mobile total coverage (a total of 45.8%).

![Placeholder](/assets/images/25k-to-30k.png)

Map 2 considers the same factors as Map 1, however, the radius was altered by 5,000 km — from 25,000 to 30,000. Although one would assume increasing the radius by a number as staggering as 5,000 would alter the results significantly, a mere 0.6% difference (41.7% total area covered by T-Mobile) was achieved. The same analysis was used: dividing the max (this time 7172600041.773993) by the sum (still 12301062346), getting a value of 58.3%. This value was subtracted by 100 to get the total area covered.


![Placeholder](/assets/images/increased-towers-10m.png)

Map 3 still follows the given parameters of the previous 2 maps, however, this map considers the difference an alteration of 10 meters in cell tower height would have on T-Mobile coverage in LA County. Interestingly, altering the tower height (as opposed to increasing the range) had a much more significant effect in cell tower coverage area. By increasing the towers’ height by 10 meters, the coverage area increased by almost 2% (a total of 43.6%). The same viewshed analysis factors were held constant: dividing the max (this time 6935051785.647749) by the sum (still 12301062346), to get the total area not covered (56.4%). This number was then subtracted by 100 to get the total area covered.