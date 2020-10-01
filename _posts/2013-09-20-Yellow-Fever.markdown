---
layout: post
title: "Modeling Yellow Fever: Propositions for Mosquito Control Program vs. Isolation & Incubation Program"
date: 2013-08-21
description: 
image: /assets/images/yellow-fever-full.png
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

### Modeling Yellow Fever Based on Kalgraf's Predictions - The Human Population

![Map GIS](/assets/images/yellow-fever-human.png)

This model is a subset of Kalgraf's original model described prior, with emhasis on the human population. The population follows Kalgraf's study of Veracruz - out of 20,000 people, 100 are ascribed the Incubated phase leaving 19,900 vulnerable.

![Map GIS](/assets/images/vulnerable-vs-sick.png)

This time series model illustrates the human population's exposure to Yellow Fever over 280 days. During the initial stages of the epidemic, there is an exponential increase in sick people as people carrying Yellow Fever are unaware in the first 4-5 days. However, as the population starts to incubate and follow proper isolation procedures, a linear decline in vulerable people appears. The amount of sick people tapers off as the amount of vulnerable people declines.

![Map GIS](/assets/images/immune-vs-deaths.png)

This time series model denotes Kalgraf's overarching goal - to model the number of people who survive Yellow Fever and become immune, versus the number of cumulative deaths. It parallels the 90% survival rate of the disease; 18,000 people are survive and become immune, and 2,000 people die.

Analyzing just the human population in Kalgraf's model allows for a more granular understanding of the implications associated with Yellow Fever outbreak rates and human recovery rates. For instance, the model assumes the amount of bites received by infected mosquitoes per day will remain constant over time. In reality, the amount of bites per infected mosquito will oscillate; as the human population begins building immunity, the rate of infected mosquitoes will decline - and so will the bites received per day. Moreover, holding the stages of Yellow Fever (incubated, contagious, and sick) at finite increments poses issues. For example, recovery rates will differ among person to person. While using Veracruz, Mexico as a case study allowed for predicting the diaspora of Yellow Fever in urban centers, and a better understanding of human recovery rate with real data, it's important to note the prevalence of the city's climate for mosquito reproduction. The tropical climate with little variation from season to season is ideal for mosquitoes. Places like Veracruz with high rates of precipitation and overall higher temperatures, will experience a greater possibility of infected mosquitoes - and therefore higher rates of bites per day. Places with similar climate's to this case study will be exposed to greater rates of Yellow Fever outbreaks.

### Modeling Yellow Fever - A Breakdown of Kalgraf's Full Model

![Map GIS](/assets/images/yellow-fever-full.png)

This is a working model of Kalgraf's diagram in its entirety. The parameters set for humans follows the nuanced modeling of the 'Human Population' segment above - initialized with 100 incubating humans, and 19,900 vulnerable humans. The emerging mosquito flow in the model represents the 27,778 mosquitoes Kalgraf predicted reach adulthood and can carry Yellow Fever. Out of the 500,000 mosquitoes, 417,000 denote 'safe mosquitoes.' The remaining 83,000 represent 'new mosquitoes.'

To better understand Kalgraf's model, a walk-through of formulas dervived through the analysis of Veracruz's Yellow Fever outbreak is provided below.

-781 people are in the Incubation Stage, 803 people are in the Contagious Stage, and 450 people are sick. The peak of the Yellow Fever outbreak occurs around day 140, with nearly 450 people becoming sick. The highest volume of deaths per day is 18 people.
-83,000 mosquitoes are characterized as 'new mosquitoes' and have the potential of carrying Yellow Fever if they come into contact with an infected human. These mosquitoes bite 0.2 people every day - a total reaching over 16,000 per day. Kalgraf predicted 4.2% of these mosquitoes will come into contact with an infected individual, making nearly 700 of these 'new mosquitoes' carriers of Yellow Fever per day.
-7,909 mosquitoes are set to the incubation stage; 1,945 are in the infectious stage. Theese 1,945 infectious mosquitoes are the catalyst for the peak in Yellow Fever outbreak on day 140.
-8,103 humans are categorized as 'vulernable' for the outbreak. To calculate the number of people contracting Yellow Fever, the following formula was used:
 # of Contagious Mosquitoes * Bites/Day * Percent of Vulnerable Human Population -> 1,945 * 0.2 * 42.6 = 166 persons per day.

The graphs below offer visual aide to Kalgraf's model through the lens of 3 scenarios: Cumulative Deaths (humans) vs Vulnerable Population, Cumulative Death during the outbreak, and Infectious Mosquitoes vs Cumulative Deaths.

![Map GIS](/assets/images/cumulative-vulnerable.png)

The model above showcases a simulation for cumulative deaths and vulnerable people during the Yellow Fever outbreak.

![Map GIS](/assets/images/deaths.png)

The model above illustrates simulated values for the number of casualities experienced during the Yellow Fever outbreak. The peak number of deaths experienced per day is 18 people, and occurs around day 140 of the 280-day outbreak.

![Map GIS](/assets/images/mosquitoes-vs-death.png)

The model above represents the number of mosquitoes carrying Yellow Fever and the number of deaths at the peak of the outbreak.

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