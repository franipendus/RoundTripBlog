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
Our final machine-learning models were to predict hotel prices and flight prices. Both models used hotel ratings, the GDP of the destination, the origin and destination locations, and the month of travel to make the prediction. The hotel price prediction also uses the flight price and vice versa. To create the models, we started by making some initial plots between some of our variables. For example, we made a scatter plot comparing flight prices to month and average hotel prices to month. We also made a boxplot for each origin and destination vs the price of the flights. From looking at these plots and seeing what variables seemed to be associated, we had a better idea as to which variables could be good predictors of flight and hotel prices. 

After our initial analysis, we realized that since we were using a mix of categorical and numerical features, we would need to create some dummy variables for categorical features such as origin, destination, and month of travel. Our analysis helped us decide that there was a reasonably strong enough relationship between our variables to build models based on them, so we proceeded with that. 

Then we combined the dummy variables with our numerical features in an array and cross validated/trained the model. Then we ran the model on the full dataset and used the line of best fit intercept and slopes to get a prediction. We ran into an issue with that where the model kept predicting negative millions for the price but after troubleshooting and checking our work, we got it to predict reasonable values. 

![](flights_resids.png)
### Residual plot for flight prices
(shows good homoscedasticity and linearity)

![](gdp_resids.png)
### Residual plot for GDP
(shows a slight pattern with the gap in the middle, which we deemed passable for now but would
like to explore the reasons for given more time)

![](rating_resids.png)
### Residual plot for hotel ratings
(shows good homoscedasticity and linearity when ignoring the outlier)

Once the model was working and passed all of the assumption checks in our residual plots, we worked on converting it to work in the app. Getting it to communicate with the database and accept user inputs was also a bit of a struggle, but overall turned out well as it functions as expected now. 

After the first model (hotel price predicting) was fully implemented, the process of implementing the second one (flight price predicting) ran much more smoothly and they are now both ready to use in the app.


## **Software Architecture:**
![](arch.png)

Our database, RoundTrip, has 19 tables and more than 3000 data entries. Our middleware, the REST API built with Flask, has 4 main sections: machine learning model, travelers, advertisers, and deal administrators. The machine learning model contains the ML model routes, as well as the functions for each linear regression prediction (including the functions to train the models). The ML model routes are used in the front end by both the System Admin who trains the models and the travelers who use the models to predict the flight and hotel costs. The travelers middleware section contains the routes that execute the actions the travelers want to perform (aside from cost predictions). The advertisers middleware section contains the routes that execute the actions the advertisers want to perform. The deal administrators middleware section contains the routes that execute the actions the deal administrators want to perform.  

## **Database Model:**
*The initial database model* : 
![](GLOBAL.png)

*The final database model*: 
![](finaldbmodel.png)

As I began to implement the app’s functionality, the model had to change. The exchange rates attribute became its own table but was later deleted since it was no longer used for machine learning predictions. The favorite flights (’favFlights’) table was also deleted for lack of impact on the UI experience since, as a frequent traveler myself, I’ve never had a favorite flight. Finally, 3 new tables were added: 
    - the main data frame (‘main_df’)
    - hotel parameters (‘hotel_params’)
    - flight parameters (‘flight_params’)
These tables are necessary for the machine learning models. The main data frame was needed for model training as it allows us to get the data needed to perform the linear regression and come up with the line of best fit for predictions. The parameters tables store the coefficients from both lines of best fit (1 table per prediction type, ie. flight prediction has its linear regression parameters stored in ‘flight_params’) and during the prediction allow us to retrieve these coefficients to apply to a new set of inputs provided by the user. 


### Presentation Link:
https://docs.google.com/presentation/d/19QlnvmbjLDo0bogDgHAWGeKj8quzH5o8jgYfyQWjT7g/edit?usp=sharing

