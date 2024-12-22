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
 * **Player2**: Player playing on away side
 * **GoalsPlayer1**: Number of goals for Player1
 * **GoalsPlayer2**: Number of goals for Player2
 * **Overtime**: Yes if the match went to overtime, No otherwise
 * **Stage**: Round-robin or Play-off
 * **Date**: Date of the tournament. For tournaments over several day, this will be the first day of the tournament.
 * **TournamentName**: Name of the tournament
