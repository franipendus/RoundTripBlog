---
title: "Indivudal Blog #2"
date: 2024-05-27
draft: false
description: "Phase II"
tags: ["authors", "config", "docs"]
authors:
  - "nalika_palayoor"
showAuthorsBadges : true
---

# Indivudal Blog #2
## Phase II Contributions

My main contribution to the second deliverable was figuring out the flight APIs. The first big thing I had to do was research what APIs we would need for our model and then find free APIs that match our goals and needs. I found a website that has about fifteen APIs related to flight data. I looked through each one of these and found which ones would be most useful for creating a machine-learning model. 

I found one API related to past flight data and one related to future flight data. I started by working with future flight data. I figured out how to get the APIs to run in the terminal; then, I transferred this to Python by using JSON.request. I worked with Erica to figure out what countries and dates to keep and then cleaned the data set using the ones we specified. After looking at the API closer, I realized that this API doesn't have future data for the past about 6 months. We decided to try using past data for our machine-learning model but use future data for our visualizations. 

I repeated the same process of figuring out countries and dates, except for the past flight data. I took some time to figure out how the new API worked and then created a clean dataset. I sent this clean data set to Erica; she combined it with her data about Hotels and GDP. Then, we worked together to make one clean data frame. 

I made a scatter plot comparing the date to the price of the flight. Lastly, Erica and I worked together to create a simple machine-learning model. 

The hardest part of this deliverable was finding the correct data and figuring out how to use the API. There was a limit on the network on how many requests per second I could make, and so this caused the code to take a long time to run. 
