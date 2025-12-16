# A proposal for a UK ranking system for riichi mahjong to inform selections for major international events
​
Please note that this document only attempts to address riichi mahjong.
​
At time of writing, the UK lacks a lively competitive scene for the MCR ruleset. The UKMA encourages MCR players to pursue the game and would address the question of selections for major MCR events as a separate issue.
​
## A re-explanation of MERS
​
For those who are interested, let's start by recapping how MERS rankings are calculated. Those who could do without the gory, mathematical detail are welcome to skip to "An examination of MERS".
​
### MERS results
​
In MERS, your result at every tournament is a number between 0 and 1000.
​
The winner of the tournament gets 1000, last place gets 0, and every other position is evenly spaced.
​
For example: if you finish 32nd out of 60, then you beat 28 out of your 59 opponents. 28 divided by 59 is 0.475, so your MERS result would be 475.
​
### MERS weights
​
Every result you achieve has a weight, determined by the tournament at which you achieve it.
​
The weight of a tournament is determined by four factors. A tournament has more weight if it:
​
1. was longer;
1. had more players;
1. had players from more countries; or
1. required qualification (which only applies to the European Championships (ERMC)).
​
### Weight decay
​
Results older than a year have their weight halved. Results older than two years no longer count.
​
### New/inactive players
​
MERS requests that players register at least 5 results to give a representative ranking.
​
Players with fewer than 5 results are given 'virtual' results until they have 5 results.
​
Each of these virtual results is a 0 (corresponding to last place) with weight 1.
​
### The two parts of the MERS ranking
​
A player's MERS ranking is calculated in two parts.
​
These parts are both weighted averages of certain sub-selections of your results.
​
'Weighted average' means multiplying each result by its weight and summing the results, before finally dividing by the sum of the weights. Thus, results with a higher weight count more.
​
### Part A - Your consistency
​
Part A is the weighted average of all of your results.
​
Additionally, a player with at least 10, 15, 20... results can leave their worst 1, 2, 3... results out of this calculation.
​
### Part B - Your achievements
​
Part B is the weighted average of your four best results.
​
### The MERS ranking
​
A player's final MERS ranking is the average of their Part A and Part B.
​
## An examination of MERS
​
MERS has been in use for almost 10 years, and was the result of collaboration between many EMA member organisations. While it's difficult to track down the reasons for every piece of the system's design, we can examine its rammifications and try to make some inferences about its goals.
​
### MERS rewards peaks and suppresses troughs
​
Good results are effectively 'double counted' in MERS. A good result pushes up both a player's part A and part B scores.
​
A bad result only brings down the part B score - and, if the player has played enough, doesn't affect the ranking at all.
​
Therefore, attending more tournaments is _usually_ a good idea in MERS.
​
### MERS pays more attention to longer tournaments
​
Longer tournaments have more weight.
​
If you do well at a 3-day tournament, that is (by and large) three times more important than doing well at a 1-day tournament.
​
The same goes for doing badly.
​
### MERS pays more attention to wins which were 'hard to win'...
​
Tournaments with more players have more weight.
​
ERMC has even higher weight.
​
Winning at these events can be seen as more difficult, and are rewarded accordingly.
​
### ...but the definition of 'hard to win' is implemented crudely...
​
The component of the weight to do with representation of different countries might also be seen as trying to identify tournaments which are 'hard to win'. After all, more countries represented should in theory mean more playstyles to overcome.
​
It is also possible that this weight component exists just to encourage collaboration, travel and exchange of ideas across the continent.
​
Regardless, it's hard to see past the fact that having more countries represented is no guarantee of a stronger field of players.
​
Same goes for the outright quantity of players. Larger tournaments might have more good players, but there's no guarantee.
​
It's difficult to properly judge this without examining the ranking of the players in the tournament. This is tricky to administer, and we would certainly want access to raw tournament data before trying to implement it.
​
### ...and MERS pays just as much attention to losses at such events
​
Even if the increase in weight for certain tournaments is trying to identify tournaments which are 'hard to win', no effort is made to account for the fact that said tournaments would also then be 'easy to lose'.
​
A bad result has exactly the same weight as a good one, even if the weight is inflated due to the supposed skill level of the opposition.
​
This leads to perhaps the most famous quirk of MERS, where many players feel discouraged from attending EMA's flagship event, the European Championships, because of the risk of suffering a low result (made more likely by the higher than average skill level at this event) with a huge weight.
​
### MERS is volatile
​
Ranking decay is very common across games and sports, and MERS implements this by reducing the weight of results with a certain age.
​
However, the implementation is once again quite crude. The immediate halving of weights or dropping of results as soon as they cross an age threshold means that a player's ranking can change quite a lot even just between one day and the next.
​
In fact, almost all countries only use MERS (if at all) twice every three years, to select players for European and World Championships. So it can be questioned whether ranking decay is really appropriate outside of this timescale.
​
### Even MERS's intricate systems sometimes don't function as expected
​
While admittedly edge cases, there are times where the selection of results for part A and part B can generate scores which are not the highest possible.
​
Consider a player with these contrived results:
​
| Result | Weight |
| ------ | ------ |
| 1000   | 1      |
| 1000   | 1      |
| 1000   | 1      |
| 501    | 6      |
| 500    | 1      |
​
This player's part A score is the weighted average of all their results, which is 650.6.
​
Their part B score is best on their four best results. But this does not consider weight. The first four results in this table are chosen.
​
Thus their part B score is (1000 \* 1 + 1000 \* 1 + 1000 \* 1 + 501 \* 6) / 9 = 667.33, for a MERS ranking of 658.95.
​
This player would much rather have the bad result with the lower weight count toward their part B.
​
If this happened, their part B would be (1000 \* 1 + 1000 \* 1 + 1000 \* 1 + 500 \* 1) / 4 = 875, for a MERS ranking of 762.8.
​
At the other end of the scale, the same thing can happen when deciding which results to drop out of your part A (if you have enough results). A player might prefer to ignore a slightly better result with a higher weight over a slightly worse result with a low weight. But, they do not get this choice.
​
## Introducing RUKRS
​
The Riichi UK Ranking System aims to resemble and iterate on MERS, maintaining its good aspects, while aiming to improve on some of its shortcomings.
​
### Focus on average hanchan scores
​
Instead of introducing an abstract result from 0 to 1000, RUKRS focuses on your average hanchan score.
​
It is hoped that this is a more tangible number to reason about.
​
### Keep rewarding peaks and suppressing troughs
​
The UKMA wishes to encourage the growth of mahjong across the UK.
​
We generally want to make it attractive to our players to play as many tournaments as they wish.
​
By promising to highlight a player's achievements and forgive occasional spots of bad luck, we encourage our players to keep chasing to better their skills.
​
### Keep paying more attention to longer tournaments
​
It makes sense that a test of your skills over more hanchan matters more.
​
Longer tournaments have more hanchan, so these naturally contribute more to your average hanchan score.
​
### Don't try to estimate opponent skill
​
Instead of imperfect implementations of estimates of opponent skill, all hanchan are considered equally.
​
We acknowledge that it would be desirable to consider opponent skill, but this requires significant effort to track. We hope that treating all hanchan equally is a simple fix which is no less viable than the existing implementation of MERS.
​
## An explanation of RUKRS
​
### RUKRS results
​
When you finish a tournament, you receive some results to contribute to your RUKRS ranking.
​
The number of results is equal to the number of hanchan in the tournament.
​
The results are all equal to your average hanchan score in the tournament.
​
Please note: individual hanchan results do not matter; only your average hanchan score for a whole tournament (in any case, EMA tournament results are only required to include the total score, so this would not be easily trackable).
​
### Result decay
​
Results older than the date when selections were made for the previous tournament of the type being selected for, no longer count.
​
For example, selections for ERMC 2030 will not consider results achieved before the selections were made for ERMC 2027.
​
(Exceptions will be made for the first set of selections occurring immediately after RUKRS is introduced.)
​
### New/inactive players
​
RUKRS requests that players play at least 50 hanchan to give a representative ranking.
​
Players with fewer than 50 hanchan are given 'virtual' results until they have 50 results.
​
Each of these virtual results is -30,000.
​
### The two parts of the RUKRS ranking
​
A player's RUKRS ranking is calculated in two parts.
​
These parts are both averages of certain sub-selections of your results.
​
### Part A - Your consistency
​
Part A is the average of the top 90% of your results, rounded up.
​
For example, a player with between 50 and 59 results may ignore their lowest 5 results.
​
### Part B - Your achievements
​
Part B is the average of your 30 best results.
​
### The RUKRS ranking
​
A player's final RUKRS ranking is the average of their Part A and Part B.
