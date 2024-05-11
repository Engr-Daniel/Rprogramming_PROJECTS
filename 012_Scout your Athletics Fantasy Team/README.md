# SCOUT YOUR ATHLETICS FANTASY TEAM

Analyze athletics data to find new ways to scout and assess jumpers and throwers.

## Project Description
If you were scouting out an athletics team, you would need to know more than just how far each person has jumped or thrown once. You want to know who is the most consistent, who fouls the least and who comes through in the clutch. And you will need to decide which aspects are most important to you so you can find the right balance.

In this R project, you will use dataframes and the `dplyr` package to find out who you should put on your team, and in doing so become the next "Moneyball" star manager of an athletics team.

## DATA
You will use performance data collated from jumps and throws events in the US from 2013-2017.

**Task 1: Read in the dataset and extract the events of interest.**

- Import the `tidyverse` package.
- Read in the `datasets/athletics.csv` dataset using `read_csv()` and assign it to `data`.
- Filter out the Women's Javelin events, drop the `Male_Femal`e and `Event` columns, and assign the result to `javelin`.
- Print out the `head` and a `summary` of `javelin`.


**Task 2: Put the data in a tidy format, where each observation is the result from an individual flight.**

- Convert `javelin` from "wide" to "long," using `Flight : Distance` as your key:value pair.
- Assign the result to `javelin_long`.
- Remove the string "Flight" from each observation in your `Flight` column, so only the flight number remains as a numeric.
- Take a look at your data by calling head.

**Task 3: For each meet an athlete competed in, we want to know the total distance covered, the standard deviation of each athlete's successful throws and the number of successful throws.**

- Filter for observations where the distance is greater than zero.
- Group the data so you can take summary statistics of each athlete's results at a given event.
- Compute the `sum of Distance, the `standard deviation of Distance` rounded to three places, and the number of non-zero rows. Assign these to `TotalDistance`, `StandardDev` and `Success`, respectively.
- View any ten rows from the middle of the data frame (i.e., do not use `head` or `tail`).

**Task 4: Use the data frame javelin to find the difference between the first three throws and second three throws for each athlete in each event.**

- Create two new columns: `early` containing the sum of first three throws and `late` containing the sum of the second three throws.
- Create another new column `diff` containing the difference between the two (late minus early).
- Examine the last ten rows.

**Task 5: Join the diff column from javelin to the javelin_totals data frame that contains the other summary statistics.**

- `left_join` `javelin` to `javelin_totals` by the `EventID` and `Athlete` columns.
- Keep the `Athlete`, `TotalDistance`, `StandardDev`, `Success`, and `diff` columns only.
- View the first ten rows.

**Task 6: Apply a function to normalize the data across aggregate statistics then compute each athlete's average for each of the normalized stats.**

- Define and assign a function called norm that operates on result.
- Assign the data frame of normalized data to javelin_norm.
- Normalize the data by applying norm to the columns listed in aggstats.
- Find the mean for each athlete on each normalized statistic.

**Task 7: Choose the weights for your statistics. Use them to calculate a total score for each athlete and choose the top five, who will reveal themselves in javelin_team. To ensure you evaluate the trade-offs in selecting your team and choose what is most important to you, the four weights must add to ten.**

- Assign your weights for `TotalDistance, StandardDev, Success, and diff`.
- Create a new column called `TotalScore` by multiplying each summary statistic by its respective `weight` and adding the products together.
- Arrange the data frame so the highest `TotalScore` is at the top.
- Save the first five rows and the columns for `Athlete` and TotalScore.

**Task 8: Create a data frame team_stats containing your players' average statistics from the javelin_totals data frame. For now, keep this in a "wide" view so you can examine how they compare to each other.**

- Filter the javelin_totals data frame to keep those rows containing your athletes. - Use the %in% operator in your filter statement.
- Take the average by using summarize_all as you did in Task 6.
- Examine team_stats. Your boss may ask you about this in the next task!

**Task 9: Create a 2 x 2 grid of plots, each showing a different aggregate statistic. Each plot should have a bar representing each athlete on your team, and a line showing the maximum and average values for that statistic from pool_stats.**

- Tidy `team_stats` by gathering the data frame into key:value pairs of `Statistic:Aggregate`. Leave the Athlete column out of the gathering.
- Use `ggplot` to plot the aesthetics: Athlete on the x-axes, Aggregate on the y-axis and fill by Athlete.
- Add a layer to create a bar plot, where stat="identity" and the bars are in the dodge position.
- Use facet_wrap to create a 2 x 2 layout based on each `Statistic`. Set `scales` to `free_y` so each facet has y-axis values appropriate to the data.
- Include your team name in the title of the plot, e.g., Sarah's Athletic Club or Grand Rapids Athletic Club.

**Task 10: The javelin match will use the average data available in the team_stats data frame against the single-event data in the javelin_totals data frame. Since you've done all the work, you're the home team. Select which three of your five players you want to send out onto the field. Use their average data in the team_stats data frame.**

- Complete the vector for `HomeTeam`. Use digits 1-5 to identify which of your three players you want to use.
- Take a look at the `AwayTeam` vector to see how we're selecting three players' results at random from the `javelin_totals` data frame to be the away team.


## Instructor:
George Perry

Sports Scientist and Entrepreneur
