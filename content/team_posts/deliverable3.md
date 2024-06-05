---
title: "Project - Deliverable 3"
date: 2024-05-27
draft: false
description: "Updates /& Advancements"
tags: ["authors", "config", "docs"]
authors:
  - "nalika_palayoor"
  - "erica_indman"
  - "frani_pendus"
showAuthorsBadges : false
---

# Project update 3

## **Updates to our phase 2 proposal:**

After looking further into data availability, users will be able to be able to get travel information when going to and from the following places: London, Paris, Rome, Madrid

## Sourced data tables:
- main_df.csv → full data set of all quarterly flight, hotel, and GDP data we collected for every combination of the four countries (sourced)
- Countries → sourced
- Airports → sourced
- Travelers → generated
- Airlines → generated
- Flights → generated
- Trips → generated
- flightBookings → generated
- dealAdministrators → generated
- hotels → sourced
- hotelBookings → generated
- favHotels → generated
- dealInfo → generated
- dealImpressions → generated
- advertisers → generated
- adInfo → generated
- adImpressions → generated



We will create two machine learning models that will be able to predict information for the users:

1.  ML model 1: Hotel cost prediciton

    -   User inputs: origin, destination, travel month, desired hotel rating, and flight cost
    -   Features/reason for choosing this feature:
        1.  Destination: Some destinations will be more expensive than others
        2.  Travel month: Some months are more expensive than others due to some months being more popular for travel
        3.  Desired hotel rating: Higher-rated hotels will tend to be more expensive
        4.  GDP: Safer places will likely cost more than less safe places

    - We will predict the cost of the hotel. We will also output the current GDP based on the month they are traveling to.

3.  ML model 2: Airline cost prediction

    -   User inputs: origin, destination, month of travel, desired hotel rating, and hotel cost
    -   Features/reason for choosing this feature:

        1.  Origin: Longer flights will cost more, and some places are more expensive to fly out of than others
        2.  Destination: Longer flights will cost more, and some places are more expensive to fly into than others
        3.  Travel month: Some months are more expensive to travel during because they are more popular months to travel in
        4.  GDP: GDP: Safer places will likely cost more than less safe places

    -   We will predict the cost of the flight. We will also output the current GDP based on the month they are traveling in.
5.  For current GDP output, we will have to hard code this because of data availability. However, past GDP values will be used to train both models

When creating the machine learning models, the first issue we encountered was that our data set felt too small to make good predictions. Although our model ran ok, we thought having more data would be better. To combat this issue, we will collect data for hotels and flights twice per month instead of once during the next phase of the project. 
 
In addition, when we ran the model the first time, it predicted a very large negative number for the hotel's cost. After playing around with the features, we figured out that we were using too many features and potentially overfitting the model. After thinking more about which features would make sense to predict price, we were able to get the model to predict a more reasonable estimate. 

## API routes:
### Travelers' routes:
* /travelers/trips/<traveler_id>
    * gets the trips of a specific traveler  
* /travelers/trips
    * updates a specific trip's start and end dates 
* /travelers/countries/<country>
    * gets a specific country's information
* /travelers/promotions/<city>
    * retrieves hotel deals for a specific city
* /travelers/favhotels/<city>/<traveler_id>
    * gets a specific traveler's favorite hotels in a specific city
* ![](d3t1.png)
* ![](d3t2.png)
* ![](d3t3.png)
* ![](d3t4.png)

### Advertisers' routes:
* /advertisers/adinfo/<advertiser_id>
    * gets all ads posted by a specific advertiser
* /advertisers/adinfospecific/<ad_id>
    * gets the ad information for a specific ad 
* /advertisers/adimp/<ad_id>
    * gets the ad impressions for a specific ad
* /advertisers/adimp/trav/<traveler_id>
    * gets all add impressions made by a specific traveler
* /advertisers/adinfo
    * posts a new ad 
* /advertisers/adinfo/<ad_id>
    * deletes a specific ad
* ![](d3a1.png)
* ![](d3a2.png)
* ![](d3a3.png)
* ![](d3a4.png)
* ![](d3a9.png)

Deal Administrators' routes:
* /dealadmin/deals/<dealadmin_id>
    * gets all deals posted by a specific deal administrator
* /dealadmin/dealinfospecific/<hotel_id>
    * gets all deals posted about a specific hotel
* dealadmin/dealimps/<deal_id>
    * gets all deal impressions about a specific deal 
* /dealadmin/dealimps/trav/<traveler_id>
    * gets all deal impressions made by a specific traveler
* ![](d3d1.png)
* ![](d3d2.png)
* ![](d3d3.png)
* ![](d3d4.png)

### ML Model Routes:
* /model/1/<v1/v2/v3/v4/v5>
    * predicts hotel price 
* ![](d3t5.png)