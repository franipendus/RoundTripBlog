---
title: "Third Blog Post"
date: 2024-06-05
draft: false
description: "Contributions To Deliverable 3"
tags: ["authors", "config", "docs"]
authors:
  - "erica_indman"
showAuthorsBadges : false
---
# Deliverable 3
## My Contributions

During this phase, I contributed to this project by data cleaning and model building. We finally figured out how to get hotel data so once that was available I cleaned it and transformed it into monthly average prices in each of our locations. After we combined all of our datasets into one main one, I began working on our model.

The model I am building is the hotel price predicting one, which currently uses flight price, hotel rating, gdp, country of origin, destination country, and quarter traveling in (last 3 as dummy variables) as predictor features because all of them would reasonably affect the price of a hotel in the country someone is traveling to. The features used may change as we refine the model, but currently they seem to predict reasonable prices for hotels. 

The biggest struggle with this model has been transferring it out of the Jupyter notebook and into pure python script.  As I was transferring it I ran into the issue that it would predict an entirely impossible price (negative millions) but still worked in Jupyter, which took a while to fix. Another struggle was learning how Streamlit works and setting up the front facing part of the model where the user will input their flight price, desired hotel rating, origin and departure location, and month of travel. Making this part interact with the backend model and formatting/scaling the inputs to match the ones that I built it with in Jupyter was another big point of struggle here. 

Besides the project, we’ve also been visiting more offices around Belgium and even some in Luxembourg. They were interesting and made me reflect on my potential future careers. Our experience visiting Health House made me interested in the intersection of data and healthcare, which I am now thinking of looking into as an area of study in the future. 

![](health_house.jpeg)
