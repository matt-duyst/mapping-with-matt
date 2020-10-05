---
layout: post
title: "Precipitation Calculations of Ski Resorts in Placer County, CA"
date: 2019-08-27
description: 
image: /assets/images/January-Interpolation.png
author: Thomas Vaeth
tags: 
  - Interpolation
---

### Intro:

This week’s challenge capitalized on two core concepts learned thus far: Interpolation (Kriging) and the multi-faceted process of building a leas-cost path. I decided to incorporate both of these lessons into a single topic—Placer County (zooming in on North Shore Lake Tahoe). I thought it would be interesting to analyze the weather patterns in the months of January and August (the typically two of the coldest and hottest months in California), and cross-reference the total accumulation of precipitation with the distance between an popular Inn (Tahoma Meadows), and 4 of Tahoe’s most common ski resorts: Homewood, Alpine, Squaw, and NorthStar. In truth, using a network analysis between the ski locations and the inn was my original thought process; however, the obtaining the OSM data was a challenge and prohibited me from using this method. A comparison with drive time between the locations (with a lens on total precipitation accumulation between the months) would have made for a better understanding of business/popularity between the two juxtaposing months. And yet, I believe creating a least-cost path (using the added factor of precipitation values with slope and water), creates a similar viewpoint for understanding Placer County just as well. I created each map originally in Arcmap, and then ran continuous simulations in Model Builder to perfect the same goal.

The first map encapsulates the process of least-cost path in its entirety: a map demonstrating the most affordable path form an origin location (Tahoma Meadows), to four counter destination locations (the 4 listed ski resorts). Considerations towards the added precipitation factor (the mean of both months divided by 2), slope, and bodies of water were accounted for. A total of 4 Digital Elevation Models were downloaded for the county of Placer were combined into a single TIFF, with a calculation for slope then undergone. The effect of water was then highlighted through a raster calculation—set with a score less than or equal to 1—to show where was water (a score of 1), and where was land (a score of 0). This slope was reclassified between two values (old and new), with ranges between 0-60 and 1-512 accordingly.

Yet another raster classification was undergone. However, this time it incorporated the newly added presence of water and slope. The original slope was added to the total amount of water and then multiplied by 128. All of the origin and destination locations were found through the website ‘Click2shp.’ After finding the cost distance, the quickest path between each points were achieved. I started with Tahoma Meadows (the origin) to Homewood, because these locations are shortest in distance. I then repeated the process 3 more times (for the other 3 ski resort locations). As a whole, Placer’s high elevation (and large presence of water that is Lake Tahoe) proved that using network analysis for this assignment would have reigned higher and better interpretable results. The paths cut through the lake—as if assuming one can swim from Tahoma Meadows to NorthStar, for instance—and doesn’t accurately illustrate the most affordable cost.

ArcScene held great value for creating the final map, because when adding an elevation gradient to the final product, a better representation was understood. Messing around with the map’s Base Heights proved this, somewhat minimizing the effect of Lake Tahoe and prioritizing the paths as the map’s main goal. The total elevation was set to a value of 5, with each layer’s offset at a degree of 50. Lighting was also toggled with through ‘3D Effects,” which gave for a final touch on this accentuation to detail.

The last two maps show the effectiveness of interpolation (kriging) for the months of January and August. Data was achieved through NOAA, and then added as XY data points in ArcMap. The second amp illustrates an interpolated range of total precipitation for the month of August, with a range between a low of 0 millimeters, and a high of 1.86 millimeters. This is to be expected in the month of August, when rain is little to none (indicated by the most common value being 0 millimeters).

As a whole, Placer’s southern places experienced the least amount of rain (0 being the average). The northern/central regions experienced a little bit more rain—Olympic Valley being towards the middle and highest northern parts like Martis Peak receiving the most The third map illustrates an interpolated range of precipitation for the month of January, with a range between 8.46 millimeters and 50.90 millimeters. Typical of California’s Mediterranean climate, Placer county’s northern region experienced larger proportions of total rainfall in the month of January than that of its southern counterpart. The largest bulk of total rainfall was in the county’s northern/central region.

### Precipitation Values: Placer County, CA

![Map GIS](/assets/images/January-Interpolation.png)

write-up

![Placeholder](/assets/images/August-Interpolation.png)

write-up

### 3D Rendering of Path Analysis to Ski Resorts in Placer County

![Placeholder](/assets/images/3d-Placer.png)

write-up