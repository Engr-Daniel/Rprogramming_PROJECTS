# LEVEL DIFFICULTY IN CANDY CRUSH SAGA
![Visual](https://github.com/Engr-Daniel/Rprogramming_PROJECTS/assets/103637488/a5ddef6c-d299-4364-98b9-e0ca5c95af21)

Analyze data from the hit mobile game, Candy Crush Saga.

## Project Description
[Candy Crush Saga](https://king.com/game/candycrush) is a hit mobile game developed by King (part of Activision|Blizzard) that is played by millions of people all around the world.

In this Project, you will get to work with a real Candy Crush dataset and use this data to estimate level difficulty. This Project assumes you can manipulate data frames using `dplyr` and make plots using `ggplot2`.


**Task 1: Load in the packages you're going to need for the project**

- readr
- dplyr
- ggplot2

**Task 2: Load in the dataset and display the first couple of rows.**

- Load the csv file located at datasets/candy_crush.csv using read_csv and assign it to the variable data.
- Display the first six rows of the data with head().

**Task 3: Count how many players are in the dataset and how many days it spans.**

- Count the number of unique players included in the data.
- Compute the period for which we have data.

**Task 4: Calculate the probability of winning a level in a single attempt for each level.**

- Group the dataset by level.
- Compute the total number of attempts and wins for each level by using the summarise function.
- Compute the probability to win as the number of wins divided by the number of attempts. Assign the result to a new column called p_win using mutate.
- The resulting data frame should be assigned to difficulty and printed out.

**Task 5: Plot a line graph with the difficulty for each level.**

- Use ggplot to plot a line graph with p_win on the Y-axis and level on the X-axis.
- Set the breaks of the X-axis to show a tick mark for every level.
- Set the Y-axis labels to a nicely formatted percentage using the scales package.

**Task 6: Add points to the plot and a horizontal dashed line at the 10% value.**

- Copy and paste the solution from task 5.
- In addition to the lines between the datapoints, add a point at each datapoint.
- Add a horizontal dashed line to the plot at Y-axis value 10%.

**Task 7: Compute the standard error of the difficulty for each level using the given formula.**

- Add the column error to difficulty which should contain the standard error of pwin using the formula error = sqrt(p_win * (1 - p_win) / attempts).

**Task 8: Add error bars to the difficulty profile plot.**

- Copy and paste the ggplot code used to generate the plot in task 6.
- Use geom_errorbar to add error bars that range from p_win - error to p_win + error for each level.

**Task 9: Calculate how likely is it that a player will complete all the levels in the first attempt.**

- Calculate the probability of the average player completing every level in the first attempt. Assign the result to p.

**Task 10: Should our level designer worry that a lot of players will complete the episode in one attempt?**

- Set should_the_designer_worry to TRUE or FALSE to indicate your answer.

## Instructor:
Rasmus Bååth

Data Science Lead at castle.io


