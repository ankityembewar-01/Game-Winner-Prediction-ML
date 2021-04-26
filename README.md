# PUBG: Game AI - Winner Prediction

##Overview
The Data science project which is given here is Game AI - Winner Prediction.This is a PUBG game Data Set. The dataset contains a large number of anonymized game stats for a single player with all match types. The target is to create a ML model which predicts players' finishing placement based on their final stats.

In a PUBG game, up to 100 players start in each match (matchId). Players (Id) can be on teams (groupId) which get ranked at the end of the game (winPlacePerc) based on how many other teams are still alive when they are eliminated. During the game, players can pick up different amunitions, revive downed-but-not-dead (knocked) teammates, drive vehicles, swim, run, shoot, and experience all of the consequences -- such as falling too far or running themselves over and eliminating themselves.

The team at PUBG has made official game data available for the public to explore and scavenge outside of "The Blue Circle." You are provided with a large number of anonymized PUBG game stats, formatted so that each row contains one player's post-game stats. The data comes from matches of all types: solos, duos, squads, and custom; there is no guarantee of there being 100 players per match, nor at most 4 player per group.

## The Goal and Insights of the project as follows:

Explore the data
Preprocessing the features
A trained model which can predict the winPlacePerc based on factors as inputs.
Dataset Description:
This file contains 128962014 individual data points in 29 columns and 4446966 rows.

groupId - Integer ID to identify a group within a match. If the same group of players plays in different matches, they will have a different groupId each time.

matchId - Integer ID to identify match. There are no matches that are in both the training and testing set.

assists - Number of times you helped your friend when he killed an enemy

boosts - Number of boost items used.
What is it ? Boost may refer to Energy Drink,Painkillers, Adrenaline Syringe
About: The boost bar is a thin white line visible above the health bar. It is cut into 4 sections, which fill up when the player uses a boost item. The first section of the boost bar lasts for 1 minute and will heal 1% health every 8 seconds, for a total of 7% health.

damageDealt - Total damage dealt. Note: Self inflicted damage is subtracted.
DBNOs - Number of enemy players knocked
What is it? Stands for 'Down But No Out'. During Duo or squad play, when you lose all your hit points(HP), you get into this mode. In this mode, your duo or squad members can heal you and that is why we don't count this as an out. 'Revive State' is a feature in BATTLEGROUNDS that can be used to revive downed squad mates. Once your HP reaches 0 you will go into a DBNO state. You can only crawl and drop items, but you cannot shoot or use items while in this state.

headshotKills - Number of enemies you killed with headshots.
heals - Number of healing items used.
About: There are three basic health items in PUBG: Bandages, First Aid Kits and Med Kits. These all restore your health bar.

killPlace - Your ranking in match in terms of number of enemy players killed.
killPoints - Kills-based external ranking of player. (Ranking where only winning matters).
kills - Number of enemy players killed.
killStreaks - Max number of enemy players killed in a short amount of time. A Killstreak is earned when a player acquires a certain number of kills in a row without dying.
longestKill - Longest distance between player and player killed at time of death. This may be misleading, as downing a - player and driving away may lead to a large longestKill stat.
maxPlace - Worst placement we have data for in the match. This may not match with numGroups, as sometimes the data skips over placements.
numGroups - Number of groups we have data for in the match.
revives - Number of times you revived your teammates.
rideDistance - Total distance traveled in vehicles (measured in meters).
roadKills - Number of enemy killed while travelling in a vehicle.
swimDistance - Total distance traveled by swimming (measured in meters).
teamKills - Number of times you are killed your teammate.
vehicleDestroys - Number of vehicles destroyed.
walkDistance - Total distance traveled on foot (measured in meters).
weaponsAcquired - Number of weapons picked up.
winPoints - Win-based external ranking of player. (Ranking where only winning matters).
Target:

winPlacePerc - The target of prediction (Target Variable). This is a percentile winning placement, where 1 corresponds to 1st place, and 0 corresponds to last place in the match.
Feature Characteristics:

int IDs to identify players, groups and matches
Discrete data about stats (assists, boosts, headshotKills)
External rankings (based off of some post-match math): ELO scores
Certain features listed as inconsistent (rankPointsElo)
