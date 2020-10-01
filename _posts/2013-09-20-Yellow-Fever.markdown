---
layout: post
title: "Modeling Yellow Fever: Propositions for Mosquito Control Program vs. Isolation & Incubation Program"
date: 2013-08-21
description: 
image: /assets/images/Yellow-Fever-Model.png
author: Thomas Vaeth
tags: 
  - Insight Maker & Model Builder
---

### Introduction:

The premise of this project is to illustrate the significance of model building and System Dynamics for epidemics - an applicable realization as the rapid spread of infectious diseases is a common trope throughout history. In fact, many epidemiologists predict that a pandemic the scale of the Spanish influenza will soon sweep the globe (Covid-19). Yellow Fever is transmitted through mosquitoes, specifically the Aedes aegypti species. Monitoring the infected is complicated; this viral disease has different impacts on each person, making predictions on the duration and severity of Yellow Fever difficult to pinpoint.

The models below simulate the proliferation of Yellow Fever through varying scenarios and mitigation techniques. While each case offers a new lens on predicting the spread of the viral disease, they all follow a similar backstory: urban diaspora. Individuals will contract Yellow Fever and bring it back to a populated urban center. If the infected person is bitten by a mosquito not carrying the disease, that mosquito will now become contagious.

These simulations are adaptations of a Dynamo model for Yellow Fever outbreaks by Kjell Kalgraf. The figure below is the blueprint for this project's modified simulations.

![Map GIS](/assets/images/kalgraf-model.png)

Kalgraf's model is based on a real outbreak of Yellow Fever in Veracruz, Mexico (1899). The  population of Veracruz was nearly 20,000 people at the time. As the viral disease swept through the urban center, many casualties were suffered - 460 people died every month at the peak of the epidemic. The model predicts the mosquito population to be roughly 500,000. Kalgraf uses this outbreak as a hypothesis of sorts; he garners data based on population sizes, lifecycle of mosquitoes, estimated bites per day, and the rates of contraction and recovery, to model the severity of Yellow Fever. Ultimately, this is shown through the comparison of cumulative number of deaths and the surviving, immune population.

The parameters set for mosquitoes are as follows. 27,778 mosquitoes emerge into adulthood per day. At the height of the epidemic, there are a total of 500,000 mosquitoes. The lifespan of a mosquito is 18 days; 4 'blood feeds' are needed throughout their lifetime. Ergo, the average mosquito feeds off 0.2 persons per day - leaving roughly 100,000 bites happening per day. It's discovered that if mosquitoes don't bite humans who are infected within their first three days, they are incapable of carrying Yellow Fever for the remainder of their lifetime. However, if mosquitoes feed off an infected person within the first 3 days (the initial period) of contracting Yellow Fever, they will carry the disease.

The parameters set for humans are a little more straightforward. A human can only contract Yellow Fever if they are bitten by a mosquito carrying the disease - it cannot be spread by another human. There are three stages to monitoring a disease: Incubation period, Contagious period, and Sick period. An infected person will enter an Incubation period (the # of days between infection and signs of symptoms) for 4.5 days. This is followed by a Contagious period of another 4.5 days, and a Sick period lasting 2.5 days. 90% of humans will recover and become immune to Yellow Fever. 

##### Modeling Yellow Fever Based on Kalgraf's Predictions:

![Map GIS](/assets/images/Yellow-Fever-Model.png)

This model is a subset of Kalgraf's original model described prior, with emhasis on the human population. The population follows Kalgraf's study of Veracruz - out of 20,000 people, 100 are ascribed the Incubated phase leaving 19,900 vulnerable.

![Map GIS](/assets/images/vulnerable-vs-sick.png)

![Map GIS](/assets/images/immune-vs-deaths.png)

##### Projected Graphings of Original Model

![Placeholder](/assets/images/Cummulative-Deaths-vs-Infectious-Mosquito.png)

write-up

![Placeholder](/assets/images/Sick-People-Simulation.png)

write-up

![Map GIS](/assets/images/Deaths-Over-Time.png)

write-up

![Placeholder](/assets/images/Vulnerable-People.png)

write-up

##### Understanding the Net-Negative Flow of the Loop Diagram

![Placeholder](/assets/images/Net-Neg-Flow-Loop-Diagram.png)

write-up

##### A Proposed Mosquito Control Program: 10-Day Simulations vs. 20-Day Simulations

![Placeholder](/assets/images/larvacide.png)

write-up

![Placeholder](/assets/images/10-Day-Sim-Mosquito-Program.png)

write-up

![Map GIS](/assets/images/20-Day-Sim-Mosquito-Program.png)

write-up

##### A Proposed Incubation & Isolation Program: 10-Day Simulation vs 20-Day Simulation vs 30-Day Simulation

![Placeholder](/assets/images/isolated-model.png)

write-up

![Placeholder](/assets/images/10-Day-Isolation.png)

write-up

![Map GIS](/assets/images/20-Day-vs-30-Day-Isolation.png)

write-up