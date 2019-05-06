# Readme

## About the dataset

The chosen dataset comes from an existing Kaggle kernel available here:<br>
__[NBA Shots Log](https://www.kaggle.com/dansbecker/nba-shot-logs)__
This Dataset contains the shot log for the NBA Regular Season 2014/2015
## Assumptions
Looking for the recipe to the best shot, among the data provided in this dataset I've spotted 4 parameters that, to me, influence the outcome of a shot the most: the Distance from the basket, the Distance from the defender, the time a hooter takes to shoot and the number of dribbles before a shot.<br>
Thus, this analysis is about the choices any player has to make before taking a shot.<br>
Basketball can be an instinctive game, but behind all that instinct and athleticism there's a big part of tactics.<br>
For sure, distance influences the result of a shot (otherwise there wouldn't be any Three Points arc...) but I think that the other parameters I've listed before play a role as well. Let's see how strong their relationship with the Field Goals Percentage (FG%) is.
## Main Findings
The data allowed us to understand how what I've highlighted as the most important parameters in the choice of a shot
- Distance<br>
- Time<br>
- Position of the defender<br>
relate to the shot result. 

### Univariate Exploration
The most important finding in this exploration was linked in the distance from the basket for the Two Points shots: it seems that the teams intentionally skip _mid range shots_ prefering _long range_ two points shots because (as shown in the Explorative Visualization) the efficiency strongly decreases when shooting from at least 5 ft from the basket.<br>
Another interesting finding is that the defender distance is a right-skewed plot both for Two and Three Points shots, but excluding the long right tail (mostly due to _out of ordinary_ events) the distribution is _almost normal_ within certain ranges of distance.
### Bivariate Exploration
In order to measure this relationship I've performed a minor change in the dataset, adding a column through which I've calculated the Field Goal Percentage for each bin into which I've fractioned the the above mentioned parameters.
For example, the distance from the basket or from the defender was performed in 1 ft wide bins, the time before a shot in 1 sec. bins or the dribbles in integer number of Dribbles.<br>
The relationship was, as expected, negative for the distance from the basket (and as mentioned before, there's an interesting _void_ in the number of _mid range_ Two Pointers) and in the Touch time.<br>
The relationship was strongly positive for what concerns the distance from the defender: NBA players are _elite_ players and the distance seems a smaller _issue_ if compared to the pressure and obstacle that a defender can create.
### Multivariate Exploration
Since the distance from the defender was the strongest relationship I've found, I want check its relationship with the FG% and the number of dribbles. The number of dribbles before a shot, itself, didn't seem to have a strong relationship with the FG%, but since the more you keep the ball the more likely you are to dribble it (due to the nature of the Game itself).<br>
The result was that both for Two and Three Pointers a minor number of dribbles and a shorter touch time lead to higher FG%.<br>
Mastering the art of 1 vs 1 is a valuable skill, but surprising your defender in order to earn some space for a good shot seems a better way to score points.
## Conclusions
What emerges is that, as expected, the Game requests speed in decision-making and execution.<br>
Two Points and Three Points shots are two different specialties which allow different preparations: _Three Pointers_ can have a higher touch time and number of dribbles before the shot and still be successful, while _Two Pointers_ require a shorter touch time due to the restricted area and the proximity of the defenders.<br>
But in both cases, don't expect a player to stand there dribbling: that's not what an NBA match will allow you to do.<br>
Keeping the ball \"still\" in the same place without moving it fast looking for an open shot decreases the chances of having a defender pressing the shooter.<br>
What seems related the most to the success of a shot, in both Two and Three Pointers, is the proximity of the defender: shooting with space and away from the pressing of the defender increases the chances of scoring.<br>
As mentioned before, the ball handling skills are important (and a player can score points thanks to their penetration and dribbling abilities) but can be used not only in a _selfish_ way, but also to distribute valuable _assists_ to allow the teammates to score points suprising the defenders and take easy shots.
### List of resources
__[Matplotlib Documentation](https://matplotlib.org/index.html)__<br>
__[Seaborn Documentation](https://seaborn.pydata.org/)__