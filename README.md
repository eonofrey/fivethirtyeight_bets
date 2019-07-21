# FiveThirtyEight vs. Vegas Odds 

David Harris came up with the idea of comparing fivethirtyeight.com's MLB predictions vs. the Vegas odds for betting. It works as follows: 


There are Vegas money lines for every MLB game of the season (below). For these games you'll see a number like +120, or -150 etc... These numbers are all based around $100 bets. A positive number, like + 120, means if you bet $100 on your team and they win, it will pay $120. For a negative money line, ex. -150, you need to bet $150 to win $100. Teams with negative money lines are the favorites, since you get a smaller payout if they win. 

You can back into an implied probability of winning with these money lines. For example, a money line of +100 means you bet 100 to win 100, so the probability of that team winning is 50%. 

The general formula for converting a money line to an implied probability is as follows: 

<img width="558" alt="Screen Shot 2019-07-19 at 9 26 42 PM" src="https://user-images.githubusercontent.com/38504767/61572454-f202c080-aa6b-11e9-8025-cb362c04f10f.png">

ESPN publishes MLB games along with the various money lines from different places where you can gamble on the games. 

<img width="913" alt="Screen Shot 2019-07-19 at 9 15 54 PM" src="https://user-images.githubusercontent.com/38504767/61572382-8e2bc800-aa6a-11e9-89ac-03f7a9bde6d2.png">

On Nate Silver's website, fivethirtyeight.com, they post every MLB game of the season along with a "Chances of Winning" column (below)

<img width="807" alt="Screen Shot 2019-07-19 at 9 15 07 PM" src="https://user-images.githubusercontent.com/38504767/61572360-50c73a80-aa6a-11e9-8f02-27202fa8abe8.png">


If you convert the money lines on ESPN to probabilities of winning, you have a direct comparison to fivethirtyeight's probabilities of winning the game. If the people of fivethirtyeight are smarter than the bookies, then a betting strategy would be to compare the fivethirtyeight probabilities vs. the implied gambling probabilities and bet on the games where there is the largest discrepancy.

This script does the following: 
1. Scrape the games with probabilities on fivethirtyeight
2. Scrape the games with money lines on ESPN
3. Convert the money lines to implied probabilities
4. Join the two tables on date and team
5. Take the difference between the probabilities and sort the table by the differences to get the games where there is the largest discrepancy

The final output is the current day's games, sorted by the difference in win probabilities between fivethirtyeight and ESPN. In the run I did on 7/21, the strategy would say to bet on the Mariners since fivethirtyeight has them at a 48% chance to win while Vegas is pricing the bets to imply only a 38% chance to win. 

<img width="824" alt="Screen Shot 2019-07-21 at 9 57 37 AM" src="https://user-images.githubusercontent.com/38504767/61592204-0646da80-ab9e-11e9-8fc0-3382ae9e31d6.png">

