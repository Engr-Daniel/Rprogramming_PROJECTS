# VISUALIZING INEQUALITIES IN LIFE EXPECTANCY

Compare life expectancy across countries and genders with ggplot2.

## Project Description
Do women live longer than men? How long? Does it happen everywhere? Is life expectancy increasing? Everywhere? Which is the country with the lowest life expectancy? Which is the one with the highest? In this project, you will answer all these questions by manipulating and visualizing United Nations life expectancy data using `ggplot2`.

## DATA
The dataset can be found [here](http://data.un.org/Data.aspx?d=GenderStat&f=inID:37&c=1,2,3,4,5,6&s=crEngName:asc,sgvEngName:asc,timeEngName:desc&v=1) and contains the average life expectancies of men and women by country (in years). It covers four periods: 1985-1990, 1990-1995, 1995-2000, and 2000-2005.

**Task 1: Load libraries and the dataset.

- Load the `dplyr`, `tidyr` and `ggplot2` packages.
- Read `datasets/UNdata.csv` into a data frame and name it `life_expectancy`.
- Print the first few rows of life_expectancy.

**Task 2: Manipulate the dataset to contain male and female life expectancy for each country.**

- Filter `life_expectancy` to obtain all records such as `Year` is equal to `2000-2005`.
- Subset the dataset to include just three columns: `Country.or.Area`, `Subgroup`, and `Value`.
- Convert `Subgroup` into two other columns called `Female` and `Male`, reshaping dataset from long to wide.
- Print the first rows of the resulting dataset.

**Task 3: Create a basic scatter plot for male vs. female life expectancy.**

- Use the `ggplot` function to initialize a ggplot object. Declare subdata as the input data frame and set the aesthetics to represent Male on the x-axis and Female on the y-axis.
- Add a layer to represent observations with points using geom_point.

**Task 4: Add reference lines and axis limits.**

- Copy your code from task 3.
- Add a dashed diagonal line that passes by (0, 0) with slope equal to 1.
- Set limit of x-axis from 35 to 85.
- Set limit of y-axis from 35 to 85.

**Task 5: Add plot titles and axis labels.**

- Add the plot title: "Life Expectancy at Birth by Country".
- Add the next caption: "Source: United Nations Statistics Division".
- Set the x-axis label to "Males".
- Set the y-axis label to "Females".

**Task 6: Annotate certain countries on the plot with labels.**

- Modify the `ggplot(...)` function to set the `label` parameter to `Country.or.Area`.
- Add a label to countries defined by `top_male`.
- Add a label to countries defined by `top_female`.
- Change the plot theme to `theme_bw`.

**Task 7: Manipulate the dataset to contain the difference in male and female life expectancy for each country.**

- Look at the first transformations already defined in the sample code.
- Convert `Sub_Year` into four other columns called `Female_2000_2005`, `Female_1985_1990`, `Male_2000_2005` and `Male_1985_1990`, reshaping dataset from long to wide.
- Create a new variable called `diff_Female` as the difference between `Female_2000_2005` and `Female_1985_1990`.
- Create another variable called `diff_Male` as the difference between `Male_2000_2005` and `Male_1985_1990`.

**Task 8: Plot the variables on the scatter plot and create axis limits.**

- Set `diff_Male` column to x-axis
- Set `diff_Female` column to y-axis.
- Set limits of x-axis from -25 to 25 using `scale_x_continuous`.
- Set limits of y-axis from -25 to 25 using `scale_y_continuous`.

**Task 9: Add reference lines to the plot.**

- Add a dashed horizontal line that passes through point y=0.
- Add a dashed vertical line that passes through point x=0.

**Task 10: Annotate certain countries on the plot with labels.**

- Create a dataset called `bottom` with bottom three rows of `subdata2` ordered by `diff_Male+diff_Female`.
- Add labels for the top three countries using `top`.
- Add labels for the bottom three countries using `bottom`.

## Instructor:
Antonio Sánchez Chinchón

Data Scientist at Telefónica