---
title: "Project - Deliverable 1"
date: 2024-05-17
draft: false
description: "Our Idea"
tags: ["authors", "config", "docs"]
authors:
  - "frani_pendus"
  - "erica_indman"
  - "nalika_palayoor"
showAuthorsBadges : true
---

# Project Proposal

The purpose of our app is to allow users to better inform themselves and plan the most cost-effective trips so that travel can be more accessible for everyone. Users can plan the best time to travel to their desired location by using our app's predictions on information about flights, hotels, and currency exchanges. Our app has a deal administrator, which allows hotel companies and airlines to add in promo deals on their chosen dates. Lastly, our app will allow third-party advertisements from any firm to generate revenue for our app. 

Our app will begin by asking the user if they want general suggestions on hotels and flights for their trip or if they want to know if their travel plan is cost-effective or not. For the former scenario, the user will be prompted to enter a location and timeframe, and using regression modeling based on past hotel and airline costs and current currency exchange rates, the user will be given a date for the travel day as well as hotel and airline suggestions. For the latter case, the user will input their desired location date of travel, and the app will tell them if their date is “good,” meaning that their plan is cost-effective compared to surrounding dates. 

By being able to choose where one wants to go and a timeframe, users are given time flexibility, which is a practical struggle for many people who have other activities going on in their lives, such as work and family. Similarly, being told whether or not a specific travel date is a “good” date to go to the inputted location allows a user to pick the most cost-effective date for their travel, saving them money and time on travel research.


# User Persona
## User Persona 1: Maria
Maria is a 22-year-old travel enthusiast from Rome, Italy. She is a student who wants to explore the world but on a budget. Her goal is to determine the cheapest time to travel to her desired country, France. 

### Stories:
- As a user, I want to be shown the most cost-effective time to travel to France so that I can save money.

- As a user, I want to be able to test a specific travel date to see if it is a good time to go (based on prices) so that I can avoid wasting money by going at the wrong time.

- As a user, I want to be recommended airlines with deals around my travel days so that I won’t miss any offers and can take advantage of them.

## User Persona 2: Gabriel
Gabriel is a 38-year-old professional at a company in Boston, USA. He is looking to buy ad space in an app with millions of monthly visitors like ours. His goal is to promote his company on an effective platform. 
 

### Stories:
- As an advertiser, I want to buy reasonably priced ad space so that my company can profit from it. 

- As an advertiser, I want my ads to be featured in frequently visited places on this site so that the amount of views and clicks is maximized.

- As an advertiser, I want to be given insights into how many clicks my ad receives on this site so that I can evaluate its effectiveness. 


## User Persona 3: Elliott
Elliott is a 56-year-old Hilton budgeting executive from London, UK. He has allocated part of Hilton’s budget to creating promos and deals to better expand Hilton’s clientele.  He aims to bring in new customers by incentivizing them to stay in the many tiers and hotels worldwide. 


### Stories:
- As a deal administrator, I want to be able to put deals out there for my hotel so that more people can come and stay here. 

- As a deal administrator, I want to see how many people have booked one of my hotels from this app so that I can measure hotel demand based on a given time of year. 

- As a deal administrator, I want to see what other hotels offer deals/promos on a given date to better evaluate competitors in the hotel market.


# Questions
* What is the best time (price-wise) to travel to a given location?
   * This is an interesting question because it allows a user to choose where they want to go and a time range when they can travel to their desired location. The user receives the best prices to go to their destination, giving them the chance to optimize their savings while traveling. Furthermore, it allows for an analysis of travel patterns that involve aspects like hotels, currency, and flights that fluctuate on a day to day basis.
* Is the user’s chosen travel date a ‘good’ time to travel? *(based on prices of surrounding times)*
    * This is an interesting question because being able to check if your chosen travel date is ‘worth it’ or not could help users make sure that they are choosing a financially conscious date to travel on. This way, they will be sure that they made a good choice, or if they didn’t, will be able to use our app to determine a better date.

# Data Sets 
* Hotels 
    * https://www.makcorps.com/ 
* Currency Exchanges 
    * https://currencyfreaks.com/#documentation
    * https://fixer.io/documentation
    * https://currencybeacon.com/api-documentation
    * https://exchangeratesapi.io/

* Flights 
    * https://rapidapi.com/obryan-software-obryan-software-default/api/compare-flight-prices/pricing 


