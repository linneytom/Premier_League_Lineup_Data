# Premier_League_Lineup_Data
Jupyter Notebook containing a spider for betstudy.com that scrapes lineup data for each game in the Premier League.

Python Libraries Needed:
requests -- Used to get html code from the betstudy.com website
bs4      -- Used to parse the html

Python Libraries Recommended:
numpy    -- Used for null values
pandas   -- Used to format data into a .csv file
tqdm     -- Used for crawling interface

The spider iterates over a table containing every game outcome in the 2018/19 season. For every row it iterates over it travels along a hyperlink that leads it to the lineup of each team for that specific game, aswell as the referees. The spider then iterates over the tables containg the lineup data and follows another hyperlink to the players profile page. From their the spider scrapes the players full name and position, it does this for the referees aswell but doesnt take their position. 


Once the data for an iteration is collected it is appended to two dictionaries one containing the player names the other the positions. After the iterations are completed (all 380 games are collected) the dictionaries are formatted into two pandas dataframes which are then saved to .csv files. A players name in the name .csv has a position in the position .csv at the same index and column as their name. 
