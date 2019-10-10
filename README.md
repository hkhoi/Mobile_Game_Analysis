# Mobile_Game_Analysis
Mobile gaming makes up nearly 75 percent of global mobile revenue during first half of 2019. A report reveals that gaming made up approximately $29.6 billion of mobile revenue. (source: https://gamedaily.biz/article/1020/report-mobile-gaming-makes-up-nearly-75-percent-of-global-mobile-revenue-during-first-half-of-2019)

As a gamer myself, I have motivated myself to analyse an open Kaggle open dataset "17K Mobile Strategy Games" that contains 16847 unique games & 16 variables to work with. (source: https://www.kaggle.com/tristan581/17k-apple-app-store-strategy-games
Data handling & Visualization done by using Python in Jupyter Notebook.

# Contents
1. Objective
2. Investigation Strategy & assumptions
3. Findings
4. Future work


## Objective
To expose the best combination for strategy games available in the appstore in order to get a good user rating (4/5 and above)

## Investigation Strategy
1. Size vs User Rating
2. Original Release date vs Size
3. Game Price and In-App Purchase Factor
4. Age Rating Factor


### Assumptions
- Games without User Rating are dropped.
- Games with less than 200 user rating are dropped. This is to prevent biased rating from developer and/or their friends' rating.
- There are about 600 unique game genre in the dataset due to different combination of genre, and sequence of genre. 
  However final genre will be only 4 types, they are:<br/>
  Puzzle (include Puzzle/Board games) <br/>
  Action, <br/>
  Adventure (include Adventure/Role playing games)<br/>
  Family (include Family/Educational games)<br/>
  
  This will cover the top 8 game genre based on below report:
  https://www.gamasutra.com/blogs/SimonHill/20141216/232458/Games_rule_the_iTunes_App_Store_Most_popular_genres_revealed.php
Game Genre and corresponding number of games in Appstore 




### Size vs User Rating
It is known mobile game developers has to take mobile phone specifications into account, as bigger games takes more resources and might not run well in lower end mobile phones. However that will limit the amount of content and graphical quality of the game.
This analysis intened to find out what are the trend of game size available as well as how good are they in terms of user rating.
![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/01%20Size%20vs%20UR.PNG)

1. From the visualization, we can see that most of the game (insert %) are below 250MB
In which to achieve score 4 and above it has to be 100MB and above. 
2. Second column of the chart shows that good games (score >4) are between 300MB to 600MB, with the exception of score 3.5 games and a small portion of score 3.0 games.
3. A very small portion of games (less than 100 titles) are above 1GB, in which the minimum score for the game is 3-3.5. This might be due to the user sentiment who gives credit to the huge game content and possibly better game graphics.
We can see that games that lies between 1.2GB and 1.7GB gets score >4.


 **Inference:<br/>
 -For simpler games, focus on size between 100MB to 150MB of contents<br/>
 -For more complex games, target between 300MB to 600MB of contents<br/>
 -Games above 1GB have good tendancy to land above 3.5 score and above, provided sufficient resource available to the developer<br/>**
  *size in the appstore and actual game size may differ after installation, patching and downloading additional content from game server*



#### Size vs User Rating by Genre
From the pie chart below we can conclude that amount of Puzzle game > Adventure > Action > Family

![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/04%20Genre%20Pie%20Chart.PNG)

A strip plot is created to analyse the Game Size vs User Rating grouped by genre

![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/03%20Game%20Size%20vs%20Genre%20by%20Rating.PNG)

We can easily say that more than half of the games from these 4 genre gets a score of 4 and above, in which the majority focuses on size 400MB and below. With the exception of Adventure which still gets good rating up to 600MB. Family (and education) genre can be further looked at by developers to avoid the intense competition to other genres which are dominating the market

**Inference: <br/>
-Puzzle games are less saturated above 400MB to achieve score 4.0 and above<br/>
-Action & Adventure Genre games are less saturated above 400MB to achieve score 4.0 and above<br/>
-Family/Educational games has less competition overall**<br/>
*size in the appstore and actual game size may differ after installation, patching and downloading additional content from game server*



### Release date Analysis
Over the 12 years, the average Game Size sure has to grow to suit advancing mobile technology as well as accomodate thirstier players.
 ![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/05%20Game%20Size%20changes%20over%2012%20years.PNG)

From the left graph we can see a almost Linear incrase of game size except a sudden spike from 2013-2014. We can also notice that the error margin has in the error bar- that means the size of game has a bigger range. We can deduce that smaller size games are still relatable but at the same time developers challenged the market with bigger size games (as big as 3.7GB per game)

The right graph shows the growth of game size per game Genre. It is noted that the Game Size fluctuates fronm year to year, but shows 
an overall trend of increasing, especially Action Genre which shows a constant growth in the last 5 years
 
 **Inference: <br/>
-Game size are increasing roughly 50MB per year with Action/Adventure games takes up bigger size and Family/Puzzle less size<br/>**
*Future work: investigation of size trend in more detail*
 
 
 
 ### Price factor 
Everyone loves free stuff, which explains the most significant amount of free and cheaper games (< $0.99 ) available in the store
 
 ![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/06%20Game%20price%20vs%20user%20rating.PNG)
 
The trend of user rating with respect to price becomes better as the game becomes pricier. We can tell that the game developers are confident and priced their games reasonably. Where games above $8.99 always scores 4.0 and above. While games below $5.99 shows a rating range of 1.5 to 5.

 ![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/07%20In%20App%20Purchase%20vs%20Game%20Price.PNG)
 
 The pricier the game gets, the higher the lower the In_App_Purchase items are. This is expected as low price and free games needs to sustain with some form of income
 
  **Inference:<br/>
-Almost 90% of the developers focuses on games below $1 and places In-App Purchase as their strategy for income<br/>
-Paid Games tend to have better reviews espeicially those above $8.99 that scores 4.0 User Rating<br/>**
 
 
 ### Age Rating Factor
Targetted Age Rating does not reflect the actual gamer's age, but plotting it against User Rating, we can see what does most of the consumer prefers: mature contents above 17+ rating

 ![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/09%20Age%20Rating%20vs%20User%20Rating.PNG)
 
However, games rated 17+ makes up for least in the dataset of 2.9%

 ![alt text](https://github.com/hkhoi/Mobile_Game_Analysis/blob/master/Image/08%20Age%20Rating%20Pie.PNG)
 
  **Inference: <br/>
-Consumers enjoy more matured content i.e games targetted for 17+ age and above**
