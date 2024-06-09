---
title: "Project - Deliverable 4"
date: 2024-05-27
draft: false
description: "Final Project!"
tags: ["authors", "config", "docs"]
authors:
  - "nalika_palayoor"
  - "erica_indman"
  - "frani_pendus"
showAuthorsBadges : false
---

# Project update 4 

## **Machine Learning Models:**

## **Software Architecture:**
![](arch.png)

Our database, RoundTrip, has 19 tables and more than 3000 data entries. Our middleware, the REST API built with Flask, has 4 main sections: machine learning model, travelers, advertisers, and deal administrators. The machine learning model contains the ML model routes, as well as the functions for each linear regression prediction (including the functions to train the models). The ML model routes are used in the front end by both the System Admin who trains the models and the travelers who use the models to predict the flight and hotel costs. The travelers middleware section contains the routes that execute the actions the travelers want to perform (aside from cost predictions). The advertisers middleware section contains the routes that execute the actions the advertisers want to perform. The deal administrators middleware section contains the routes that execute the actions the deal administrators want to perform.  

## **Database Model:**
*The initial database model* : 
![](global.png)

*The final database model*: 
![](finaldbmodel.png)

As I began to implement the app’s functionality, the model had to change. The exchange rates attribute became its own table but was later deleted since it was no longer used for machine learning predictions. The favorite flights (’favFlights’) table was also deleted for lack of impact on the UI experience since, as a frequent traveler myself, I’ve never had a favorite flight. Finally, 3 new tables were added: 
    - the main data frame (‘main_df’)
    - hotel parameters (‘hotel_params’)
    - flight parameters (‘flight_params’)
These tables are necessary for the machine learning models. The main data frame was needed for model training as it allows us to get the data needed to perform the linear regression and come up with the line of best fit for predictions. The parameters tables store the coefficients from both lines of best fit (1 table per prediction type, ie. flight prediction has its linear regression parameters stored in ‘flight_params’) and during the prediction allow us to retrieve these coefficients to apply to a new set of inputs provided by the user. 


### Presentation Link:
https://docs.google.com/presentation/d/19QlnvmbjLDo0bogDgHAWGeKj8quzH5o8jgYfyQWjT7g/edit?usp=sharing

