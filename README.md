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
1. Genre vs User Rating
2. Size vs User Rating by Genre
3. Ori Rel date vs User Rating
4. Ori Rel date vs User Rating by current version
5. Language vs User Rating
6. Language vs User Rating by Genre
7. In app purchase vs User Rating
8. In app purchase vs User Rating by Genre
9. Age rating vs User Rating
10. Age rating vs User Rating by 
11. Dev type (enterprise vs personal)

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
