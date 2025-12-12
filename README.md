# League of Legends First Turret Analysis and Win Predictor
In this project I analyze a League of Legends(LOL) 2025 dataset from Oracles Elixer. This was conducted as a final project for DSC80 at UCSD focusing on the impact of destroying first turret and how other related features affect the outcome of a game.


Author: Nicholas Chan


# Introduction

League of Legends is a popular multiplayer online battle arena game launched in October 2009 by Riot Games. It has since become one of the most popular multiplayer games and has a big esports scene. The dataset that I worked with contains data from professional esports matches that took place throughout 2025. 

This dataset contains key information about each match that was played. The dataset captures the teams and individual players performances, the outcome of the match, and timestamps of certain in-game statistics. 


In a game of League of Legends, I believe that the team who gets **first tower** gains a significant advantage over the other. Destroying first tower opens up the map and allows for more team play, better objective control, and in general allows you to pressure the opponent more. This leads to the main interest of my project, how accurately can we predict the outcome of a game know which team got first tower. Further more I will investigate how much more we can improve this model by including features available to us at the 15 minute mark of a game.


The dataset contains a wide summary of each professional esports match played with the metrics totaling to 118932 rows and 164 columns of unique data. I decided to only keep the rows that summarized the teams performance, since the goal is to predict the outcome of the game we dont really care about each individuals performance. For the sake of our analysis we are only interested in a couple of these columns. Here is an introduction to the columns that I will be using:

- `side` : The side of the map the team played on, Red or Blue

- `firstblood`: Binary column indicating if the team attained first blood

- `firstdragon`: Binary column indicating if the team attained first dragon

- `firsttower`: Binary column indicating if the team destroyed first tower

- `firstmidtower`: Binary column indicating if the team destroyed first mid tower

- `firsttothreetowers`: Binary column indicating if team was the first to destroy 3 towers

- `turretplates`: The number of turret platting achieved by the team

- `opp_turretplates`: The number of turret platting achieved by the opposing team

- `golddiffat15`: The difference in gold attained at 15 minutes

- `killsat15`: The number of team kills at 15 minutes

- `csdiffat15`: The difference in team creep score at 15 minutes

- `xpdiffat15`: The difference in team xp at 15 minutes

- `assistsat15`: The teams number of total assists at 15 minutes

- `void_grubs`: The number of void grubs achieved by the team


# Data Cleaning and Exploratory Data Analysis

