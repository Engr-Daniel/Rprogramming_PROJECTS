# IMPORTING AND CLEANING DATA

Apply your importing and data cleaning skills to real-world soccer 

## Project Description
Your boss at Crunching Numbers needs you to determine which match and stadium had the highest attendance during the 2019 FIFA Women's World Cup. Use your data import and cleaning skills to dig through the dirty data, clean it up, and present your boss with polished graphs.

## DATA
These data come from the online 2019 FIFA Women's World Cup [match reports](https://www.fifa.com/womensworldcup/matches/?#groupphase).


**Task 1: Load the packages and read in the data.**

- Load the `readr` and `dplyr` packages.
- Read in the data from the datasets folder using `read_csv()` and assign it to the variable, `wwc_raw`. The name of the data file is `2019_WWCFIFA_summary.csv`.
- Determine the class of `wwc_raw` and its dimensions. Use `glimpse()`, `summary()`, and `str()` to look its structure.

**Task 2: Import data and assign data types.**

- Use `read_csv()` to read in the data again. This time parse `Round` to factor, `Date` to date, and `Venue` to factor by setting the `col_types` argument.
- Inspect the data by calling `glimpse()` and `summary()`.
- The dataset is not large - print it and explore.

**Task 3: Change all column names to lowercase and remove rows of NA.**

- Load the `tidyr` package.
- Create `wwc_1` by first changing all column names to lowercase, then removing rows of `NA`.
- Get the dimensions of `wwc_1`, then inspect the first ten and last ten rows.

**Task 4: Find the NA and replace them with correct data.**

- Using `which()` and `is.na()`, find the index value for the `NA` in the date column of `wwc_2` and assign it to `index_date`. Use `[]` to subset and view the row with the missing data, then replace the `NA` with the correct data value (given).
- Repeat the process for `venue`.

**Task 5: Separte data in columns and replace NA.**

- Create `wwc_3` from `wwc_2` by calling `separate()` twice, and then calling `replace_na()` twice within `mutate()`. Separate score into `home_score` and `away_score`. Separate `pks` into `home_pks` and `away_pks`. Replace the `NA` in `home_pks` and `away_pks` with 0.
- Print the data and marvel at your awesome data cleaning skills!

**Task 6: Create a boxplot to look for outliers.**

- Load the `ggplot2` package.
- Using `wwc_3`, create a boxplot of `attendance` by `venue` using `geom_boxplot()`. The first line of code is the call to `ggplot()` with the correct `x` and `y` aesthetics. The second line of code is the call to the boxplot geometry. Do not forget the `+`.

**Task 7: Summarize the attendance at each venue and fix the outlier.**

- Summarize the number of games, minimum attendance, and maximum attendance at each venue in `wwc_3`.
- Use `mutate()`, and `which()` within `replace()`, to update the outlier with the correct value, `57900`. Assign the updated dataset to `wwc_4`.
- After updating the outlier, summarize the number of games, minimum attendance, and maximum attendance **at each venue** and print the summary table.

**Task 8: Redo the boxplot from Task 6. This time make it prettier.**

- Add the correct geometries to create a boxplot of the attendance by venue. Add red, jittered points over the boxplot. Reduce the size of the points to `0.5`.
- Within `labs()`, add a title, `"Distribution of attendance by stadium"`, and a subtitle, `"2019 FIFA Women's World Cup"`.

**Task 9: Make a line plot of venue attendance over the duration of the tournament.**

- Add the correct x and y aesthetics and color each line by `venue`.
- Add the correct geometry to make a line plot.

**Task 10: Answer the following multiple-choice questions.**

- Which match had the highest attendance during the tournament?
- In what stadium was the match with the highest attendance played?


### Instructor: 
Erin LaBrecque

Instructor at DataCamp