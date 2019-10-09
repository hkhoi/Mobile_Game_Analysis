# Mobile_Game_Analysis
Mobile gaming makes up nearly 75 percent of global mobile revenue during first half of 2019. A report reveals that gaming made up approximately $29.6 billion of mobile revenue. (source: https://gamedaily.biz/article/1020/report-mobile-gaming-makes-up-nearly-75-percent-of-global-mobile-revenue-during-first-half-of-2019)

As a gamer myself, I have motivated myself to analyse an open Kaggle open dataset "17K Mobile Strategy Games" that contains 16847 unique games & 16 variables to work with. (source: https://www.kaggle.com/tristan581/17k-apple-app-store-strategy-games

# Contents
1. Objective
2. Investigation Strategy & assumptions
3. Findings
4. Future work


## Objective
To expose the best combination for strategy games available in the appstore in order to get a good user rating (4/5 and above)

## Investigation Strategy
1. Size vs User Rating
2. Size vs User Rating by Genre
3. Ori Rel date vs User Rating
4. Ori Rel date vs User Rating by current version
5. Language vs User Rating
6. Language vs User Rating by Genre
7. In app purchase vs User Rating
8. In app purchase vs User Rating by Genre
9. Age rating vs User Rating
10. Age rating vs User Rating by 
11. Developer type (enterprise vs personal)

### Assumptions
- Games without User Rating are dropped.
- Games with less than 200 user rating are dropped. This is to prevent biased rating from developer and/or friends rating.
- There are about 600 unique game genre in the dataset due to different combination of genre, and sequence of genre. 
  However final genre will be only 4 types, they are:
  Puzzle (include Puzzle/Board games)
  Action 
  Adventure (include Adventure/Role playing games)
  Family (include Family/Educational games)
  
  This will cover the top 8 game genre based on below report:
  https://www.gamasutra.com/blogs/SimonHill/20141216/232458/Games_rule_the_iTunes_App_Store_Most_popular_genres_revealed.php
Game Genre and corresponding number of games in Appstore 
Puzzle (72,316)
Action (65,249)
Family (58,370)
Educational (45,452)
Adventure (38,943)
Strategy (26,671)
Board (25,165)
Simulation (21,729)
Trivia (17,091)

### Size vs User Rating
It is known mobile game developers has to take mobile phone specifications into account, as bigger games takes more resources and might not run well in lower end mobile phones. However that will limit the amount of content and graphical quality of the game.
This analysis intened to find out what are the trend of game size available as well as how good are they in terms of user rating.
![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/01%20Size%20vs%20UR.PNG)

1. From the visualization, we can see that most of the game (insert %) are below 250MB
In which to achieve score 4 and above it has to be 100MB and above. 
2. Second column of the chart shows that good games (score >4) are between 300MB to 600MB, with the exception of score 3.5 games and a small portion of score 3.0 games.
3. A very small portion of games (less than 100 titles) are above 1GB, in which the minimum score for the game is 3-3.5. This might be due to the user sentiment who gives credit to the huge game content and possibly better game graphics.
We can see that games that lies between 1.2GB and 1.7GB gets score >4.

### Size vs User Rating by Genre
From the histogram below we can conclude that amount of Puzzle game > Adventure > Action > Family
(note: the sum of game here is much less than original dataset 17k titles is due to the filter out of no rating/low rating count and less mainstream games genre as mentioned in assumptions section)
![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/02%20Number%20of%20games%20by%20genre.PNG)

A strip plot is created to analyse the Game Size vs User Rating grouped by genre

![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/03%20Game%20Size%20vs%20Genre%20by%20Rating.PNG)

We can easily say that more than half of the games from these 4 genre gets a score of 4 and above, in which the majority focuses on size 400MB and below. With the exception of Adventure which still gets good rating up to 600MB
