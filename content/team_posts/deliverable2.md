---
title: "Project - Deliverable 2"
date: 2024-05-27
draft: false
description: "Updates /& Advancements"
tags: ["authors", "config", "docs"]
authors:
  - "frani_pendus"
  - "erica_indman"
  - "nalika_palayoor"
showAuthorsBadges : false
---

# Project Updates
### Data availability

Due to sourcing data, our app is now going to be a price of trip predictor based on yearly quarters and only from the following **Locations/Airports**: 
* London, United Kingdom 
    * LHR- London Heathrow Airport
* Paris, France 
    * CDG- Charles de Gaulle Airport
* New York, USA
    * JFK- John F Kennedy Airport
* Barcelona, Spain 
    * BCN- El Prat Josep Tarradellas Airport
* Rome, Italy 
    * FCO- Leonardo da Vinci–Rome Fiumicino Airport
* Berlin, Germany
    * BER- Berlin Brandenburg Airport
* Brussels, Belgium
    * BRU- Brussels-Zaventem Airport

The user will input a date and we will predict the price of that trip based on quarterly gdp data, flight and hotel prices. 

### Interesting questions
We changed our interesting questions to be: 

* What is the best time (price-wise) to travel to a given location?
    * This is an interesting question because it allows a user to choose where they want to go and a time range when they can travel to their desired location. The user receives the best prices to go to their destination, giving them the chance to optimize their savings while traveling. Furthermore, it allows for an analysis of travel patterns that involve aspects like hotels, currency, and flights that fluctuate on a day to day basis.

* How safe is the user’s intended destination?
    * This is an interesting question because keeping track of world events can be hard with the current state of international relations, specifically among countries that are currently at war and their supporters. Having an easy way to check this would be beneficial to travelers since they need to know if they will be safe in their destination.

* What offers/deals are available and when?
    * This is an interesting question because it allows advertisers and administrators to see what kinds of ads and offers their competitors have as well as the timing of those offers. It allows for a better business strategy for both parties as well as benefits a user who can save money in this way and discover new aspects related to their trip. 

### User persona 
We modified the storoies of Maria, User Persona 1, to include a concern over safety:
- As a user, I want to be able to check the travel advisory score of my destination so that I can be safe while traveling abroad. 

### Data 
Linked below are our new data sets for ML modeling:
- Hotels: https://xotelo.com/
- GDP: https://data-explorer.oecd.org/vis?lc=en&tm=quarterly%20gdp&pg=0&snb=41&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_NAMAIN1%40DF_QNA_EXPENDITURE_CAPITA&df[ag]=OECD.SDD.NAD&df[vs]=1.0&lo=5&lom=LASTNPERIODS&dq=Q............&ly[rw]=REF_AREA&ly[cl]=TIME_PERIOD&to[TIME_PERIOD]=false&vw=tb
- Safety: https://www.travel-advisory.info/data-api
- Flights: https://developers.amadeus.com/self-service/category/flights/api-doc/flight-cheapest-date-search/api-reference



# Project Advancements

### Data visualization 
![](dm2.jpeg)
![](dm3.jpeg)
![](dm4.jpeg)

### Preliminary ML model
![](def1.png)
![](def2.png)
![](def3.png)
![](ml1.png)
![](ml2.png)
![](ml3.png)

### Localized ER diagrams 
![](travelers.png)
![](ads.png)
![](dealAdmins.png)

### Global ER model 
![](GLOBAL.png)

### SQL for global data model 
https://github.com/franipendus/roundTrip/blob/main/databaseInit.sql
