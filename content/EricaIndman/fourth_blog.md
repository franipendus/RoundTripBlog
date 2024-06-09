---
title: "Fourth Blog Post"
date: 2024-06-08
draft: false
description: "Contributions To Deliverable 4"
tags: ["authors", "config", "docs"]
authors:
  - "erica_indman"
showAuthorsBadges : false
---
# Deliverable 4
## Contributions, Challenges, and Highlights

In this final phase of the project we implemented our models into the app code and worked on getting them to function with user input, communicate with the database, and display results to the user. There were definitely many struggles with this, but it works in the end and it is satisfying to see the results of our project.

When I coded the model in Jupyter it was easy to pass information into it as the dataframe with all the information was right there, but getting it to work in the app was a challenge. I wrote pseudo code first to plan out how user inputs would be converted and standardized and then worked with Frani to figure out how to communicate with the database to pull out the necessary data and store the results of the training function which we would later use to predict. 

Since some of our features are categorical, (month, origin, and destination) they had to be converted to dummy variables in order to be used for linear regression, so I made a logic path to turn those inputs into usable forms, such as an origin of ‘London’ being converted to [0,0,0]. For the numerical features, we called the database for the relevant columns (flight cost, hotel cost, hotel rating, GDP) and I got the means and standard deviations of them to standardize each user input. This is so that the user can input real world values and the different scales (for example a normal flight price being 300 but ratings being on a 1-5 scale) would not interfere with the accuracy of the model. 

This stage is where I had the most trouble when the model kept returning impossible predictions (negative millions). I spent a while on debugging and checking my work over and over, only to realize that the issue was that I wasn’t standardizing one of my variables. Once I caught that it worked, and the experience showed me the importance of standardization in prediction modeling, and also attention to detail. 

Then, I made an array of all the user inputs and then we called the database again to retrieve the parameters array which we previously stored. This array included the intercept and all the slopes of the line of best fit that was produced from training this model on our dataset. Lastly, I did the dot product of these arrays to produce the value which would be returned to the user as the predicted hotel price once it was sent through the paths. This was the most enjoyable part of the project, as seeing it all come together with the DS modeling side working alongside the CS app/database side was rewarding and made us feel like we actually produced something real. 

Besides finally finishing this project, the other highlight of this week was the soccer game that we went to and got to cheer for Belgium at. I’ve never been to a soccer game and generally don’t go to sports games at all (besides horseback riding competitions) so it was a new experience for me and I’m glad I got to do it abroad and have fun with it!

![](game.jpeg)

This whole experience was so great and even though it felt like a fever dream sometimes I can definitely say I learned so much here and before taking this class I never would have thought that I would be able to do the things I've done for this project. Being in Belgium made it even better and I know I'm going to miss it so much when I leave, I'm so grateful for this opportunity. 

## Resume Section:

### Projects
#### RoundTrip Project, May 2024 - June 2024

- Developed a web app with my team members centered around affordable, accessible travel and price predicting.

- Worked with Python, Pandas, Numpy, Flask, and Streamlit.

- Was responsible for collecting and cleaning data from multiple public APIs, and then using it for building, testing, and implementing a multi-variable linear regression model from scratch that predicts hotel prices based on user inputted origin, destination, date, and flight cost.
