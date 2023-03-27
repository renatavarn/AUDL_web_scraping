![AUDL logo](https://github.com/renatavarn/AUDL_web_scraping/blob/main/AUDL%20logo.png)


# American Ultimate Disc League (AUDL) - a web scraping project

Scraping data from the [AUDL website](https://theaudl.com/) to extract player stats and personal info for the 2022 season into a single table. 

## Workflow: 

1. `Scrape player stats`: combine 50 pages of the stats tables for 2022 statistics from the [Player Stats](https://theaudl.com/stats/player-stats?year=2022) website. 
2. `Extract player URLs`: from the scraped player stats table, extract invidual player websites. E.g. the first player in the list is Ryan Osgar and this is his [personal AUDL page](https://theaudl.com/league/players/rosgar). 
3. `Scrape personal player pages`: loop over the extracted URLs and create a separate dataframe with player info including age, height, weigth, jersey number and college. 994 players in total so this step takes a LONG time (around 2 hours)!
4. `Clean and merge tables`: clean the resulting player stats and player info tables merge them into a single data frame based on players name. 

## Required libraries: 
<img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white" /> 
<img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" />

BeautifulSoup 
RegEx  

## Variables in the final dataframe: 

Personal info:
Name, Team, Age, Height_cm, Weight_kg, Jersey_no, College

Player statistics (cumulative or %): 
Posessions, Total scores, Assists, Goals, Blocks, +-, Completions, Cmp% (completion percentage), Yards, Throwing Yards, Receiving Yards, Offensive Effic, Hockey assists, Throwaways, Stalls, Drops, Calahans, Hucks, Huck completion %, Pulls, Offensive PP, Defensive PP, Minutes played


### Feel free to download `audl_2022_player_data.csv` file and do your own analysis! It can be used for comparing individual players or teams during the 2022 season and more.

