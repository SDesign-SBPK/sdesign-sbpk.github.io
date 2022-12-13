---
layout: post
title:  "Site Setup - Catchup Log"
date:   2022-10-20 11:23:49 -0400
---

First post on the site. This is serving as a catch up of all the previous activities in the semester regarding the project. Going forward, these should be more frequent and smaller logs of what is happening for the project.

## September

September was all about trying to figure out a project that everyone wanted to work on and would be interested in. All of the group have different interests in computer science, so there was some difficulty with finding something interesting for all. Initial ideas included the following:
- A sports prediction app that used health data of players to predict long-term outcomes based on current actions
  - This project was one that everyone was interested in, but was abandoned due to difficulties in retrieving health data
  - The sports prediction aspect was carried over into the current project 
- A remote power/start-up device that would handle turning on a dormant device and helping to locate it
  - This project was also one that all members were interested in, but was left due to the many similarities to Tile Trackers and Airtags
- A food produce life-extender that would live in a produce drawer and detect the different levels of gas released by ripening produce. The device would then be able to absorb some of the gas and connect to an app that would warn users about different items in the drawer going bad
  - The project was abandoned due to a lack of review from professors and a lack of interest from all team members
- Rephoto is an extension on a project that Dr.Pless had originally completed. The project would have extended it to be used in a variety of use cases 
  - The idea was overlooked due to the desire to do something original

After deciding on an idea, we completed a project proposal for review. Feedback to the proposal was largely focused on the need to scale down. We originally wanted to create an app built around the prediction engine but that would also include social aspects, potential betting, or as a prediction for multiple different leagues. Based on the feedback, we switched the league being focused on (Club Frisbee to AUDL) due to the availability of data and simplified the project to use the prediction engine and make hypothetical matchups available between players and teams in different conditions and locations.

At the end of the month, we completed a practice presentation of the executive summary to the class. Feedback included the desire to expand the project beyond the simplifications made due to the project proposal feedback. We decided to embrace the fantasy elements, as suggested, and included fantasy teams and matchups in future plans.

## October - So Far

October began actual development on the project. Work was divided into four initial areas:
- Database design and deployment
- AUDL data scraping
- Weather API research and data retrieval
- ML research and preliminary algorithm design

Each of the four areas has (currently) progressed well, with all four areas projected to be completed by the end of the month. The month has largely been about laying groundwork for the next month and a half. We want to make sure that we are setting ourselves up enough to complete a functional product by the end of November/early December, with the alpha prototype demo on December 9. Going forward, we will focus on setting up the ML algorithm (a neural network) with Tensorflow or Keras to be able to make some kinds of initial predictions with either one or two weather factors or individual player data in 1-on-1 matchups.

Additional other aspects that need to be fully setup include an AWS server. This will serve in the future as the end deployment server and we would also like to have all of the data available at all times on a server that is fully available to the members of the team. A software request document was submitted, but no response has been given.