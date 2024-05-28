---
title: "Second Blog Post"
date: 2024-05-27
draft: false
description: "Contributions To Deliverable 2"
tags: ["authors", "config", "docs"]
authors:
  - "erica_indman"
showAuthorsBadges : false
---
# Deliverable 2
## My Contributions

In this phase of the project my main contributions were API sourcing, reading, cleaning, and plotting. I also started our machine learning model to make a proof of concept. Most of the APIs I read in are not yet reflected in our plots and code but will be used later. 

I made a dataframe with information like Country, GDP, and Quarter. This will be merged with the current Flight dataframe that we worked with for this deliverable, and will be used to flesh out our linear regression model. I am also working on adding hotel prices to this and we will use those to return a predicted hotel price along with the predicted flight price for the user’s trip.

I used plotly and seaborn to plot the relationships between some of the columns in our Flight dataframe that Nalika collected and I also fit a simple linear regression model to the Date and Price columns. These will be used to explore the relationships between our data and help us choose which factors will be most useful in predicting flight and hotel prices. 
