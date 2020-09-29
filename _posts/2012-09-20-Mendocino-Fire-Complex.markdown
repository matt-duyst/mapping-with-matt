---
layout: post
title: "Mendocino Fire Complex: Calculating Surface Vegetation Fluctuations through Spectral Indices (NDVI & NBR)"
date: 2012-09-20
description: 
image: /assets/images/Posterboard.png
author: Thomas Vaeth
tags: 
  - Remote Sensing
---

### Introduction:

This research delves into the complexities associated with measuring fire’s impact on an ecosystem, through the scope of vegetation health and re-growth. This study explores fluctuations in the condition of surface vegetation, the Normalized Difference Vegetation Index (NDVI), of Mendocino County before, during, and after the emersion of the Mendocino Fire Complex. In addition, burn severity was calculated through the spectral index of the Normalized Burn Ratio (NBR), which utilizes reflectance data directly before and shortly after the emergence of a fire.

The Mendocino Fire Complex was California’s largest wildlife in state history, and was comprised of two fires: The Ranch Fire and the River Fire. It consumed over 450,000 acres. The Complex surfaced on July 27th, 2018 and persisted until its containment on October 4th, 2018. The continuation of the Complex is most likely attributed to California’s Mediterranean climate.

### Methods:

Two Landsat TM images were obtained before the Complex emerged, and after it was contained (Path 45 Row 33: July 10; Path 45 Row 32: July 10; Path 45 Row 32: October 30; Path 45 Row 33: October 30).

Normalized Differenced Vegetation Index (NDVI) was utilized for its accentuation on regions of chlorophyll that exhibit the highest rates of reflectance and absorption. NDVI is calculated by the following formula: (NIR-RED)/(NIR+RED). The resulting change in NDVI values was obtained from subtracting the post-fire values with the before-fire values.

Normalized Burn Ratio (NBR) estimates burn severity and highlights burned regions. NBR is calculated by the following formula: (NIR-SWIR)/(NIR+SWIR). By subtracting the post-fire image with the pre-fire image, the dNBR image is obtained. The images were calibrated to the top-of- atmosphere (TOA) reflectance, and radiometrically calibrated to account for brightness temperature. This allowed for clouds and shadows to be removed from the images.

### Results:

### Mendocino Fire Complex

![Map GIS](/assets/images/Mendo-GIS.png)

Illustrated above are the two fires that account for the Mendocino Fire Complex (The Ranch Fire and the River Fire), as well as the boundaries of the Mendocino National Forest and Mendocino County. Major roads and rivers are also represented.

##### NDVI Analysis - Before Fire

![Placeholder](/assets/images/Before-NDVI.png)

This map illustrates the Normalized Difference Vegetation Index (NDVI) values across the (future) burned areas of the Mendocino Complex on July 10th, 2018. These values are derived from Landsat 8 imagery provided by USGS Earth Explorer.

##### NDVI Analysis - After Fire

![Placeholder](/assets/images/After-NDVI.png)

This map illustrates the Normalized Difference Vegetation Index (NDVI) values after the Mendocino Complex
on October 30th, 2018. These values are derived from Landsat 8 imagery provided by USGS Earth Explorer.

##### NDVI Analysis - Total Vegetation Change

![Placeholder](/assets/images/Total-NDVI.png)

This map illustrates the calculated change in Normalized Difference Vegetation Index (NDVI) values across the burned areas after the Mendocino Complex’s dissipation. It was calculated by finding the difference of post-fire NDVI values and pre-fire NDVI values. These values are derived from Landsat 8 imagery provided by USGS Earth Explorer.

##### NBR Analysis

![Placeholder](/assets/images/NBR.png)

This map illustrates the calculated change in Normalized Difference Vegetation Index (NDVI) values across the burned areas after the Mendocino Complex’s dissipation. It was calculated by finding the difference of post-fire NDVI values and pre-fire NDVI values. These values are derived from Landsat 8 imagery provided by USGS Earth Explorer.

### Discussion:

As predicted, Mendocino County experienced high NDVI values prior to the Complex, and a substantial decrease in NDVI values after the Complex. NDVI values prior to the Complex on July 10th were moderately high, taking into account the effect of California’s mediterranean climate. The lack of precipitation in the year 2018, coupled with intensified temperature values during the dry summer season, explain for the pre-complex mean NDVI value of 0.33, post-complex mean NDVI value of 0.08, and total change mean NDVI value of -0.24.

The goal of this research was to unveil the changes in vegetation cover over the Mendocino National Forest and surrounding areas in Mendocino County, after the surfacing of California’s largest wildfire in state history: The Mendocino Fire Complex. This was achieved through analyzing the difference in vegetation cover change by comparing NDVI values with the spectral indices of NBR. Pre-fire vegetation experiences high NIR reflectance and low SWIR reflectance, while post-fire vegetation experiences low NIR reflectance and a high SWIR response. The region’s overall high dNBR values illustrate an intense burning, with seldom areas experiencing negative values and the associated increase in vegetation regrowth. Seasonal variations were outside the scope of this research, due to the relatively small change in spectral signatures during California’s dry period (from July to August).


### Acknowledgements:

I would like to personally thank Dr. Nick Burkhart for being my advisor during the curation of my independent research. I would also like to thank Geoffrey Fricker for sharing his knowledge of advance remote sensing techniques, and his continued interest in my academic and professional fields related to GIS.

Sources: GeoMac, USGS Earth Explorer, USGS UN-SPIDER, USDA National Forest, US Census Bureau 2018 TIGER/ Line, the California Natural Resources Agency National Hydrology Dataset (NHD).


