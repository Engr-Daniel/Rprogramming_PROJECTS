# DRUNKEN DATETIMES IN AMES, IOWA

Apply your skills from "Working with Dates and Times in R" to breathalyzer data from Ames, Iowa.


## Project Description
In the [Who Is Drunk and When in Ames, Iowa?](https://www.datacamp.com/projects/208) project, you looked at breathalyzer test data from the State of Iowa. There was a lot of date-time manipulation that was hidden behind-the-scenes in that dataset. In this project, you will proceed to uncover temporal trends in the Ames breath alcohol data.

Anyone with familiarity with the `lubridate, dplyr, and ggplot2` packages will be able to complete this project successfully. You will manipulate the dates and times in the breath alcohol data to answer questions such as, `"What day has the most tests?"`, `"at which hour of the day are breath alcohol tests most common?"`, and `"are blood alcohol content (BAC) results higher on days when Iowa State University's football team plays?"`


**Task 1: Begin working with this data by creating a bar chart of number of tests by day of the week.**

- Load the `tidyverse and lubridate` packages.
- Read `"datasets/breath_alcohol_datetimes.csv"` into the workspace using `read_csv`, and save it as `ba_dates`. 
- Change the timezone of the DateTime to `"America/Chicago"`.
- Using `wday()`, create a column in ba_dates called `wkday`, the weekday of the test. Set label = TRUE to extract Sun, Mon, etc. labels.
- Create a bar chart for the ba_dates data using `geom_bar()` with wkday on the x-axis.

**Task 2: Look at the hour of the day for weekend days only and look at side-by-side bar charts for these three days by hour of the day.**

- Create a column in `ba_dates` called `hr`, the hour the `DateTime` variable. Use `hour()`.
- Make a new data frame, `weekend`, by filtering ba_dates to include only tests from Friday, Saturday, and Sunday.
- Using the `weekend data`, create side-by-side bar charts (for each weekend day) of number of tests by `hr` of the day using `facet_grid()`.

**Task 3: After rounding the time of the test to the nearest date, summarize by date and plot some time series.**

- Use the `round_date` function to round the `DateTime` column to the nearest day, creating a date column in ba_dates.
- Use the `count` function to count up the number of tests per date and save the result as `ba_summary`.
- Pipe `(%>%)` the `ba_summary` data into a `ggplot` command that uses `geom_line()` to make a time series plot.
- Use `scale_x_date()` to create labels on the x-axis every `"6 months"`.

**Task 4: Read in the football game data, and subset the `ba_summary` data to contain only the dates when Iowa State's football team played.**

- Read in `"datasets/isu_football.csv"` using `read_csv()`. Save it as `isu_fb`.
- Make the Date column a date object with `parse_date()`. Supply the correct date format to format.
- Filter the `ba_summary` data to include only the dates in `isu_fb`. Save it as `ba_fb`.
- Arrange `ba_fb` so that the date with the most breathalyzer tests is shown first. Print the first six rows.

**Task 5: Join the `ba_summary` data to the `isu_fb` data and create a visualization showing the difference in breathalyzer test counts between wins, losses, home, and away games.**

- Do a `left_join()` to join ba_summary to `isu_fb`, creating the object isu_fb2.
- There are several game dates with no breathalyzer test data. Use `mutate` and `ifelse` to change the NAs to 0s.
- Create a bar chart with `n` on the x-axis. Fill by `Home` and facet by `Res` (the game result) to see the conditions with the most breathalyzer tests.

**Task 6: Extract the month of each date in the ba_dates data and create visualizations of the number of tests by month and year.**

- In `ba_dates`, create a column `mo` using the `month()` function and a column yr using the year function.
- Create a bar chart of number of tests per month.
- Create the same bar chart again but color the bars according to year. Use `as.factor(yr)` to color the bars as a categorical variable, not a numeric variable.

**Task 7: Create time intervals for the weeks during VEISHEA and for similar weeks in other years, then see which year has the most tests given.**

- Use the `make_date()` and `interval()` functions in lubridate to create time intervals for the VEISHEA weeks in 2013 and 2014. In 2013, VEISHEA was held from April 15-21. In 2014, it was held from April 7-13. Don't forget about the timezone!
- Create a data frame `veishea` by using the `%within%` and `filter()` to select only the `ba_dates` in a VEISHEA week.
- Using `count()`, count the number of breathalyzer tests during each VEISHEA week.

**Task 8: Compute the mean BAC result and draw a ridgeline plot for the result by hour of the day.**

- Using mutate(), create a column in ba_dates called res that is the mean of Res1 and Res2.
- Load the ggridges package.
- Draw the ridgeline plot so that res is on the x-axis and one density ridge is drawn for each hour.

**Task 9: Count the number of tests with breath alcohol reading of zero, then create another ridgeline plot that excludes zeroes.**

- Create an indicator variable in `ba_dates` called `zero` that is TRUE when `res` is 0 and is `FALSE` otherwise.
- Tabulate the `zero` variable with the `count` function.
- Recreate the previous ridgeline plot with data that has been filtered to exclude the zero values.

**Task 10: Subset the data to contain tests with results greater than 0.31, and examine the time of day they occurred.**

- Create a new data frame, `danger`, that contains `res` of at least 0.31.
- Print `danger` and examine the dates and times of these tests.


## Instructor:
Samantha Tyner

Postdoctoral Research Associate at Iowa State University