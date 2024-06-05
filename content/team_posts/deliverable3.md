---
title: "Project - Deliverable "
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
- Airlines → generated
- employees → generated
- customers → generated
- inventory_transaction_types → generated
- inventory_transactions → generated
- invoices → generated
- order details → generated
- order_details_status → generated
- orders → generated
- orders_status → generated
- orders_tax_status → generated
- privileges → generated
- products → generated
- purchase_order_details → generated
- purchase_order_status → generated
- purchase_orders → generated
- sales_reports → generated
- shippers → generated
- strings → generated
- suppliers → generated

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

Hotels: https://www.kaggle.com/datasets/mykhailozub/500-hotels-from-airbnb-booking-and-hotelscom/versions/
- Purpose: Contains information on hotels (such as rating, cost, type, etc.) for numerous European countries. We pulled the necessary data for our 4 countries. 

GDP: https://data-explorer.oecd.org/vis?lc=en&tm=quarterly%20gdp&pg=0&snb=41&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_NAMAIN1%40DF_QNA_EXPENDITURE_CAPITA&df[ag]=OECD.SDD.NAD&df[vs]=1.0&lo=5&lom=LASTNPERIODS&dq=Q............&ly[rw]=REF_AREA&ly[cl]=TIME_PERIOD&to[TIME_PERIOD]=false&vw=tb
- Purpose: Contains past quarterly GDP data for many countries. We are using the 2023 data to help train our ML models. We won't be able to use this API to output the current GDP values because it only contains past GDP data. 

Flights: https://developers.amadeus.com/self-service/category/flights/api-doc/flight-cheapest-date-search/api-reference
- Purpose: Contains possible flights for traveling to and from numerous places. We pulled the data for all combinations of the places we needed. 









