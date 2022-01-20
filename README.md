# Baseball Player Management System

## What is this?
This project is a warehouse for baseball player management that may be used by a manager or General Manager to inform
decisions related to creating a roster and deciding lineups for a matchup. 

It includes functionality for lineup comparison, matchup customization, dynamic lineup generation, player comparisons,
salary information, and in-depth breakdowns of individual player performance.

Each of these is intended to be used in tandem with each other so that a manager may gain more insight about their own
players and their opponent's players.

## Methodology
The largest unique factors to this project are the weighted game functionality and consequentially the newly calculated 
metrics that get generated from this type of aggregation.

This project uses an inverse distance formula to dynamically weight each player's performance based on the specified
date. This allows us to evaluate a player's current capabilities as a function of their more recent games, while still
acknowledging previous performances.

These weighted statistics are then aggregated to compute new metrics such as a weighted batting average, weighted on 
base percentage, weighted runs created, and weighted runs created per game. The calculations for these metrics can be
found in data_cleaning_and_organization/gen_stats.py.

Recommended lineups are based on the weighted runs created per game statistic because it considers all available
batting stats for each player, and puts all players on a level playing field in regard to the number of games they
played.

The remainder of this project leverages the weighted statistics and other raw data to generate insights about player and
team performance that would be of interest to team executives.

## How to Run
In a terminal, navigate to the game_files folder that houses the main.py file

Run the command 'python main.py' from this directory and the program will execute
