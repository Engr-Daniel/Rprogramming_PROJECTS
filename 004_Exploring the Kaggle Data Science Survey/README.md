# EXPLORING THE KAGGLE DATA SCIENCE SURVEY

Discover the top tools Kaggle participants use for data science and machine learning.

## Project Description
When beginning a career in data science, one often wonders what programming tools and languages are being used in the industry, and what skills one should learn first. By exploring the 2017 Kaggle Data Science Survey results, you can learn about the tools used by 10,000+ people in the professional data science community.

Before starting this project, you should be comfortable manipulating data frames and have some experience working with the `tidyverse` packages `dplyr`, `tidyr`, and `ggplot2`.

## DATA

This project uses a subset of the [2017 Kaggle Machine Learning and Data Science Survey](https://www.kaggle.com/kaggle/kaggle-survey-2017?utm_medium=partner&utm_source=datacamp.com&utm_campaign=ml+survey+case+study) dataset. If you want to know more about the tools and techniques Kaggle participants use, check out the full [report of the Kaggle 2017 survey results](https://www.kaggle.com/amberthomas/kaggle-2017-survey-results?utm_medium=partner&utm_source=datacamp.com&utm_campaign=ml+survey+case+study).


**Task 1: Load the data and look at the first 10 responses.**

- Load the tidyverse package.
- Using read_csv, load datasets/kagglesurvey.csv and assign it to the variable responses.
- Print the first 10 entries of responses.

**Task 2: Split the tools each respondent uses into separate rows.**

- Print the tools and languages used by the first respondent (found in column 2: WorkToolsSelect).
- Create a new data frame called, tools, by using str_split() to split the WorkToolsSelect column at the commas, then unnest() the new column to fill work_tools.
- View the first 6 rows of tools.

**Task 3: Find the number of respondents that use each language or tool.**

- Create a new data frame, tool_count, by grouping the tools data by work_tools, then use summarise() to calculate the number of responses within each group.
- Sort tool_count so that the most popular tools are at the top.
- Print the first 6 results of tool_count.

**Task 4: Create a bar chart that displays tool popularity.**

- Use ggplot2 to create a bar chart of work_tools in the tool_count data frame. Use fct_reorder() to arrange the bars so that the tallest are on the far right.
- Rotate the bar labels 90 degrees.

**Task 5: Calculate the number of respondents that use R, Python, and both tools.**

- Create a new column called language_preference which should be set to:
  - "R" if WorkToolsSelect contains "R" but not "Python".
  - "Python" if WorkToolsSelect contains "Python" but not "R".
  - "both" if WorkToolsSelect contains both "R" and "Python".
  - "neither" if WorkToolsSelect contains neither "R" nor "Python".
- Print the first 6 rows of debate_tools.

**Task 6: Calculate total number of users that use R, Python, or both, and plot the results.**

- Group debate_tools by language_preference and then use summarise() to calculate the number of each response.
- Remove the rows of respondents that use "neither" R nor Python.
- Create a bar chart of language preference counts using ggplot.

**Task 7: Find language recommendations for users that use R, Python, or both languages.**

- Group debate_tools by language_preference and LanguageRecommendationSelect. Summarise the number of recommendations for each language within each group and include only the top four most common recommendations for each language preference.

**Task 8: Create a faceted plot showing the top four language recommendations from users of R, Python, both, and neither.**

- Use the ggplot function facet_wrap() to create a faceted plot of recommendation frequency. You should get four sub-plots, one for each type of value in the language_preference column.


### INSTRUCTOR:
Amber Thomas

Journalist-Engineer at The Pudding


