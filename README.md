# Scorpion-scraper
 Scrapes all matches from Scorpion, which is a site with table hockey results. The different files used are described below:

 ## tournament_urls.txt
 This file contains the slugs to all the stages that has been scraped already. 

 ## create_data.ipynb
 Jupyter notebook that scrapes all matches from tournament stages that has not been scraped already, i.e are not in tournament_urls.txt

 ## th_matches.csv
 CSV file with all the matches. Contains the following columns:
 * **StageID**: The ID of the stage the match was in. The link to the stage can easily be created using this column in the following way: http://th.sportscorpion.com/eng/tournament/stage/{StageID}/matches/
 * **Player1**: Player playing on home side
 * **Player1ID**: Player ID of player playing on home side
 * **Player2**: Player playing on away side
 * **Player2ID**: Player ID of player playing on away side
 * **GoalsPlayer1**: Number of goals for Player1
 * **GoalsPlayer2**: Number of goals for Player2
 * **Overtime**: Yes if the match went to overtime, No otherwise
 * **Stage**: Round-robin or Play-off
 * **RoundNumber**: Represents the round number of a match. For playoff matches, RoundNumber will be set to a numeric value (e.g. 0.25 for quarterfinal).
 * **PlayoffGameNumber**: For playoff matches only. Indicates the specific game within a best-of-X series (e.g., Game 1, Game 2, etc.).
 * **Date**: Date of the tournament. For tournaments over several day, this will be the first day of the tournament.
 * **TournamentName**: Name of the tournament
 * **TournamentID**: ID of the tournament. The link to the tournament can easily be created using this column in the following way: https://th.sportscorpion.com/eng/tournament/id/{TournamentID}
 * **StageSequence**: Which sequence of the tournament the stage is. Basic groups is usually sequence 1, followed by final groups and playoffs.

## scorpion_players.csv
Unique list of Player IDs with corresponding Player Names.
