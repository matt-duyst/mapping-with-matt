---
layout: post
title: "Statewide Precipitation Averages in the Month of August: California"
date: 2019-08-26
description: 
image: /assets/images/California-August-Interpolation.png
author: Thomas Vaeth
tags: 
  - Interpolation
---

### A State on Fire: Statewide Interpolation Mapping of California in August

![Map GIS](/assets/images/january-interp-ca.png)


![Map GIS](/assets/images/California-August-Interpolation.png)

![Map GIS](/assets/images/kriging-august.png)


This week delves into two primary interpolation methods: IDW and Kriging. Because the methods are derived from simulations, these general trends that can alter from one another—even though the values remain constant. The temperature values for the months of January and August were accessed from NOAA, added as XY data, and then manipulated into the above maps in ArcGIS.

As one would expect with California’s Mediterranean Climate, temperatures in the winter-time like the month January are cooler with more precipitation than those of the hotter temperatures in the summer-time, like the month of August. The range of January was between 36°F and 72°F, while the range for the month of August was between 62°F and 114°F. January’s lowest average temperature was in Sunnyside-Tahoe City (39°F), and the month’s highest average temperature was in Mecca (72°F). This follows the trend of Northern California having a cooler climate than that of Southern California, where these two juxtaposing cities resides. August’s lowest average temperature was in Westhaven-Moonstone (63°F), and the month’s highest average temperature was in Furnace Creek (114°F).

The first two maps utilized the IDW interpolation method to create a quantile-based representation of temperature in the state of California. In my opinion, the last map (which used the Kriging Bayesian method) is more accurate in representation. For instance, the range of temperature in the month of August was altered from 62°F to 59°F. Moreover, while the distribution of temperatures appears less rigid and lends itself to a cleaner representation. To me, this method proves a more accurate reading of temperatures and relies less on generalizations like that of IDW. I chose to use the IDW method for the first two maps—the highs of January and the highs of August—to illustrate the contrast with Kriging. I think it’s interesting that the generalized results of interpolation do not precisely follow the data retrieved from NOAA. For instance, the map of January states that the lowest recorded temperature value was 36°F, whereas the actual data (shown in the graphs) states that the lowest recorded value was actually 34°F. While the physical data is a few degrees off, the trend itself is clear and reliable.
