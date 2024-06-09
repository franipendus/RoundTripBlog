---
title: "Individual Blog #4"
date: 2024-06-09
draft: false
description: "Final Project"
tags: ["authors", "config", "docs"]
authors:
  - "frani_pendus"
showAuthorsBadges : false
---

# Individual Blog #4
![](soccer.jpg)

For the final project, and since my last blog post, I contributed by building the front end of the app and creating the api routes, and implementing the machine learning models in the app. I have written more than 14 api routes with at least one from each category ('get', ‘delete’, ‘post’, ‘put’), some of which were calls to the database that immediately displayed to the data while others were used to allow users to choose specific inputs then used in other routes (ex. an advertiser picking one of their ad ids from a dropdown so that they can delete that ad). 

In my opinion, the 'get' and 'delete' routes were easy to implement and worked almost immediately; however, the 'post' and 'put' were VERY difficult for me and required a lot of time due to the string formatting, specifically pertaining to dates. It took me around 3 hours of staring at the code and getting help to realize I was missing a couple *single* quotation marks. I also found that implementing the machine learning model to properly connect to the front end was difficult because of how the returned data was formatted. In the front end pages section, I needed the ML return data to be a float since it is a cost and I needed to round it to 2 decimal places. I had to figure out how to pull a specific value out of the data dictionary and then create a float out of it. This one task took many hours of debugging and help from Dr. Fontenot who is probably still sick of me asking for help with that. 

In the end, it did work out and it was so gratifying to see the code I wrote "behind the scenes" performing tasks the user wanted on the app. I think my favorite feature I implemented was the map on the travelers/countries page as it is both interactive and different and allowed me to dip my toes into using streamlit-folium. Overall, I really enjoyed being able to see the impact my code has; in the past, I haven’t made a project that integrated this many aspects of computer science together like creating databases, learning SQL, learning python, and designing something someone other than myself (or another CS person) can actually use. 

In terms of the dialogue ending, I am truly baffled that we are done. I feel like this trip has been somewhat of a fever dream and passed by in the blink of an eye. It is so amazing to look back at myself from the start of the project and see how much I have learned and experienced in just four weeks. My highlight from this last week was most definitely the football (soccer) game. Although I am not an avid soccer watcher, I loved being in the stadium and surrounded by hundreds of cheering (and sometimes booing) Belgians. At the game, I saw a different aspect of Belgian culture which only made me love this experience more. I also saw the most incredible red and orange sunset that genuinely took my breath away. I am so grateful to have been a part of this dialogue as I will remember the people and experiences for the rest of my life. 

![](sunset.png)

### Resume
![](franires.png)