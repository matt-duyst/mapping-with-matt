---
layout: post
title: "Comprehending the Range of North Korea's Strongest Missiles"
date: 2014-09-13
description: 
image: /assets/images/Hwasong-16.png
author: Thomas Vaeth
tags: 
  - SQL & Buffer Analysis
---

### Intro:

These are 3 maps that illustrate various ranges of North Korea’s longest ranging missiles: The Hwasong-14 (1,553 miles), an Intermediate Ballistic Missile (2,299 miles), and the Hwasong-16 (8,000 miles). Each missile’s range is denoted by a buffer, which is ascribed the distance of the missile’s range. Additionally, each map showcases which country is within range of North Korea’s 3 missiles (highlighted in red). The major cities—ranked by having a population of 5 million and higher—are further displayed on each map.

The 3 missile ranges were found online vis-à-vis Wikipedia. A world country shapefile was provided through the UCLA GIS Geoportal. North Korea (highlighted in dark red) was isolated by a query builder on the world county shapefile; North Korea was then exported as a shapefile. Three buffers were created around North Korea: The Hwasong-14 (1,553 miles) missile, an Intermediate Ballistic Missile (2,299 miles), and the Hwasong-16 (8,000 miles). Each buffer was converted from decimal degrees to miles. To isolate the countries that intersect within the range of these buffers, a select by location tool was used. A world city shapefile was then downloaded from the UCLA GIS Geoportal. To isolate the major cities, a query builder was performed to isolate the cities labeled as ‘Rank 1’ (a population of 5 million or higher). These countries are labeled in blue. 


### The Varying Impact of North Korea's 3 Strongest Missles

![Map GIS](/assets/images/Hwasong-14.png)

The first map displays the range of North Korea’s Hwasong-14 missile, which reached a distance of 1,553 miles. The countries at risk within this radius are Russia, Mongolia, China, South Korea, Japan, Vietnam, the Northern Mariana Islands, and the Philippines. The Major cities within this range are Beijing, Seoul, Tokyo, Taipei, Hong Kong, and Manila (labeled in blue). 

![Placeholder](/assets/images/Intermediate-Ballistic.png)

The second map displays the range of one of North Korea’s Intermediate Ballistic missile, which reached a distance of 2,299 miles. With an expanded radius of 746 miles, there are 14 additional countries at risk: Kazakhstan, Kyrgyzstan, Nepal, India, Bhutan, Bangladesh, Myanmar, Laos, Thailand, Vietnam, Cambodia, Malaysia, Brunei, Palau, Guam, and parts of Micronesia. Moreover, 4 new major cities fall within the Intermediate Ballistic missile’s range: Lahore, Delhi, Mumbai, Bangalore, and Bangkok.

![Placeholder](/assets/images/Hwasong-16.png)

The third map displays the range of North Korea’s Hwasong-16 Missile, which reached a distance of 8,000 miles in orbit. If launched, the Hwasong-16 would reach every continent but South America. It is North Korea’s longest tested missile. The new major cities at risk would entail Moscow, Tehran, Karachi, Baghdad, Cairo, Istanbul, London, Lagos, Kinshasa, New York and Mexico City. The only major cities not at-risk are in South America, namely Bogota, Lima, Rio de Janeiro, Sao Paulo and Buenos Aires.