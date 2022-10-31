---
layout: post
title:  "End of October"
date:   2022-10-30 11:23:49 -0400
categories: jekyll update
---

The end of October means that the first sprint in the project is being wrapped up. Overall, the first sprint was largely about setting up all of the necessary pieces for future development. This includes database design, data scraping for both AUDL and weather, and research into the future structure of the prediction algorithm.

## Data Scraping

Data scraping was broken into two different pieces - AUDL and weather data. Each piece represents the data sourcing of the fundamental parts of the algorithm.

### AUDL Data

AUDL data was scraped by Brandon. 

After tracking network requests on the AUDL Stats page, backend links were found that returned all of the necessary data for AUDL sites to function. At least six different endpoints were found that took in various parameters to get data. After creating scripts to make continous HTTPS requests to the backend, several thousand JSON files were returned containing various data points about players and teams. 

The JSON files were parsed to get accurate pieces of information about different categories - overall player and team stats, player and team stats per year, and player and team stats per game. After parsing the data, it was then verified and checked to make sure that it had all the pieces needed for the future as well as had a standard format that could be used to shortcut storage and retrieval later.

### Weather Data

Weather data was researched by Philip. 

After finding many options, listed <a href = "/docs/assets/Weather_API_Research.pdf" target = "_blank">here</a>, the Visual Crossing API was decided upon due to its high amount of accuracy and easy access to historical data. 

Weather data was then scraped by using the API to get weather data for each game at specific fields. This involves tracking down the specific field location that a game was played at and getting the weather at specific times - a game is broken up into multiple intervals, to handle weather changing from the start of a game to the end of the game. The other key weather aspect that is retrieved is information about the average conditions at the location of each time. This provides information about the usual conditions that each team is used to, specifically to handle non-game playing time for players. Each team practices multiple times a week and does so in specific conditions. By looking at the regular conditions during practice, we can use this data to get an idea of the conditions that the team is used to.

## Database Design

Database design and setup was completed by Samuel. 

After looking through the structure of the returned JSON files during the AUDL data scraping, some initial relationships were found that could be used when storing data. As a result, a few initial tables were added to store data about players, teams, and various games. Subtables were added that broke stats into a per-game basis for both players and teams.

To incorporate the weather data right into the database, additional tables were added to store the location that teams play on and to hold the specific data about an interval during a game. The complete outline (for this stage) can be seen below.

![Preliminary Database Design](/docs/assets/db_diagram.png)

To assist in streamlining the design process, the Sequelize ORM was used to define the models and relationships between each. This also allows for all of the database to be interacted as if it was just regular Javascript objects. The database is able to be built locally for each developer, but we would like to have a centralized version that can have all of the data in it when doing future development. To accomplish this, we will be deploying this onto an AWS EC2 instance. This will serve us during developmenet, but will also be where we eventually deploy the final product. The server has not been set up yet, as we are still waiting for AWS credits from the instructional team. The software request document was submitted on October 9, but we have not heard anything back regarding being able to get these funds. We can deploy onto some alternative servers or possibly get some free credits from other sources, but long term goals requires getting the credits from the instructional team.

## Algorithm Research

Research for the algorithm was completed by Karim.

Multiple options were looked at to see what the best possible implementation would be. The findings from Karim's research can be found <a href = "/docs/assets/Potential_Machine_Learning_Algorithms.pdf" target = "_blank">here</a>. Overall, a neural network was found to be the best implementation to focus on, due to its high scalability and its use in other kinds of sports prediction algorithms. Looking into implementation options for neural networks revealed the Tensorflow and Keras API as the best, as outlined <a href = "/docs/assets/Neural_Network_Implementation_Research.pdf" target = "_blank">here</a>.

## Other

Besides each of the four areas worked on throughout the month, we also made some decisions about what to focus on in the next month or two. We will start development on a front end (built with React), a backend (built with Node.js), and two different machine learning models (one focusing on team aspects, the other on player aspects). Both of these will be built with the Tensorflow and Keras API, as found in the algorithm research. The models will be kept separate to see which one has a higher degree of accuracy and can compute predictions faster, with the intention of incorporating them later and giving greater preference to the better performing model.

For class assignments, we completed the first two presentations for the class. 

Presentation 1 was for the executive summary. Following the feedback from the practice round of the presentation, we pivoted to include a fantasy element after the instructional team and other members of the class showed interest in it. The presentation was not great, due to a lack of detail about specific areas and no mockups of the app presented. Feedback to the final presentation was very negative, including the contradicting feedback about the fantasy elements being uninteresting to audiences despite the direct feedback to embrace the fantasy element two weeks prior. 

Presentation 2 was for the technical summary. There was no practice round and was just completed on Wednesday, so we have not gotten feedback yet at this point. Generally it went well, though we did go over the allotted time (it seems like many teams did). 

Writing 2 was completed individually today, so each person has a different submission.