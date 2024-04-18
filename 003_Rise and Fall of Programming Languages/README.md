# RISE AND FALL OF PROGRAMMING LANGUAGUES

Analyze the relative popularity of programming languages over time based on Stack Overflow data.

## Project Description
How can you tell what programming languages and technologies are used by the most people? How about what languages are growing and which are shrinking, so that you can tell which are most worth investing time in? One excellent source of data is [Stack Overflow](https://stackoverflow.com/), a programming question and answer site with more than 16 million questions on programming topics. By measuring the number of questions about each technology, you can get an approximate sense of how many people are using it. In this project, you'll use open data from the [Stack Exchange Data Explorer](https://data.stackexchange.com/) to examine the relative popularity of languages like R, Python, Java and Javascript have changed over time.

**Task 1: Instructions**
Load the dataset and the packages required to analyze the dataset.

- Load the readr and dplyr packages.
- Load the dataset; datasets/by_tag_year.csv into a variable named by_tag_year using the read_csv() function (not read.csv()).
- Print by_tag_year.

**Task 2: Instructions**
Create a new column that for each tag-year combination contains the fraction of questions in that year that have that tag.

- Use mutate() to add a column called fraction to by_tag_year, representing number divided by year_total. 
- Name the new table by_tag_year_fraction.
- Print by_tag_year_fraction.

**Task 3: Instructions**
Filter for R tags.

- Use filter() to get only the observations from by_tag_year_fraction that represent R, saving them as r_over_time.
- Print r_over_time.

**Task 4: Instructions**
Load the visualization packages and plot fraction of R tags of overall questions over time with a line plot.

- Load the ggplot2 package.
- Plot r_over_time with year on the x-axis and fraction on the y-axis. Add a geom_line() layer to the plot to create a line plot.

**Task 5: Instructions**
Filter for the observations where tag is R, dplyr, or ggplot2, plot their fraction of overall questions over time with a line plot.

- Combine the tags "r", "dplyr" and "ggplot2" into a vector named selected_tags using c().
- Use filter() on by_tag_year_fraction, along with the %in% operator, to get only the subset of tags in selected_tags. Name the new table selected_tags_over_time.
- Visualize the popularity of these three tags with a line plot in ggplot2 (with year on the x-axis and fraction on the y-axis) using color to represent tag.


**Task 6: Instructions**
Find and sort the total number of questions for each tag.

- Use the group_by() and summarize() verbs on by_tag_year to find the total number of questions for each tag, saving the column as tag_total. - Then use the arrange() verb to sort the table in descending order of the tag_total column. Save the result to sorted_tags.
- Print sorted_tags.

**Task 7: Instructions**
Filter for the largest tags and plot them on a line plot.

- Use the filter() verb to filter by_tag_year_fraction only for the tags in highest_tags, which are the six largest tags.
- Create a line plot of the fraction of questions each of these tags made up over time, using color to represent the tag.

**Task 8: Instructions**
Filter for specific tags then plot their fraction of overall questions over time with a line plot.

- Combine the tags "android", "ios" and "windows-phone" into a vector named my_tags using c().
- Use filter() on by_tag_year_fraction to get only the subset of tags in my_tags. Name the new table by_tag_subset.
- Visualize the popularity of these tags with a line plot in ggplot2 (with year on the x-axis and fraction on the y-axis) using color to represent tag.


#### INSTRUCTOR:
David Robinson

Principal Data Scientist at Heap