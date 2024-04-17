# DATA SCIENCE FOR SOCIAL GOOD:CRIME STUDY
Use data science to catch criminals, plus find new ways to volunteer personal time for social good.

![image](https://github.com/Engr-Daniel/Rprogramming_PROJECTS/assets/103637488/6aabaa11-376a-4630-a357-95477e6fd8e0)

## Project Description
Quantitative analyses can have a significant impact on initiating change within one's community. When analyzed responsibly, data can provide evidence to understand difficult social issues correctly. In this project, you will leverage publicly available data to interpret crime patterns within the city of San Francisco.

### DATA
The dataset used in this project is [hosted on Kaggle](https://www.kaggle.com/san-francisco/sf-police-calls-for-service-and-incidents) and updated daily. Note - some of the original column names are altered for adherence to a standard naming scheme.


#### Task 1: Instructions
Prepare your environment by loading packages and data.

- Load the tidyverse and lubridate packages.
- Using read_csv() load datasets/downsample_police-department-incidents.csv and assign to the variable incidents.
- Using read_csv() load datasets/downsample_police-department-calls-for-service.csv and assign to the variable calls.


#### Task 2: Instructions
Inspect the data and generate a frequency statistic.

- glimpse() the incidents and calls datasets to understand their structure.
- count() the number of reported incidents by Date and rename the column of counts to n_incidents. Assign the output to daily_incidents.
- count() the number of civilian calls for police service by Date and rename the column of counts to n_calls. Assign the output to daily_calls.


#### Task 3: Instructions
Join the datasets by date.

- Use inner_join() to join daily_calls to daily_incidents and assign the output to a variable named shared_dates.
- Inspect the new data frame structure.


#### Task 4: Instructions
Reshape the data and visualize the trends for incidents and calls on the same graph.

- Create a "long format" data frame called plot_shared_dates from the shared_dates data frame by using gather(). Name key = report and value = count.
- Use ggplot() to visualize Date vs. count of plot_shared_dates, and color by report. Overlay a linear model to visualize trends in the data.


#### Task 5: Instructions
Calculate the correlation coefficient between the frequency of incidents and calls.

- Determine the correlation between the daily number of incidents and the daily number of calls in shared_dates. Assign the output to daily_cor and print it.
- Create a new column, month, from the Date column of shared_dates, and group_by() this new column in order to summarize() new frequency counts.
- Calculate the correlation coefficient between monthly frequencies. Assign to a new variable monthly_cor and print.


#### Task 6: Instructions
Filter the incidents and calls data frames by their shared_dates.

- Use semi_join(), a filtering join, to subset the calls dataset.
- Make sure the sanity check prints TRUE in order to ensure you are using the semi_join() function appropriately.
- Use a filtering join to subset the incidents dataset.


#### Task 7: Instructions
Rank the top call and incident crime types by frequency and visualize with a histogram.

- Subset the top 15 crime types of calls_shared_dates in descending order by count and use the pipe to pass this information to ggplot() and visualize using geom_bar(stat = "identity").
- Subset the top 15 crime types of incidents_shared_dates in descending order by count and use the pipe to pass this information to ggplot() and visualize using geom_bar(stat = "identity").
- Output the saved plots.



#### Task 8: Instructions
Compare the top locations of stolen vehicles to civilian reports of stolen vehicles.

- filter() for the appropriate crime type in calls_shared_dates and count() the location of the address variable. Assign the output to location_calls.
- filter() for the appropriate crime type in incidents_shared_dates and count() the location of the address variable. Assign the output to location_incidents.
- Print the top 10 locations for each dataset to compare.

#### Task 9: Instructions
Visualize a 2D density plot on a map of San Francisco.

- Load ggmap.
- Read in a preprocessed map of San Francisco as sf_map.
- Use filter() to subset incidents_shared_dates by grand theft auto and save this data frame as auto_incidents.
- Use ggmap() to plot the map of San Francisco, and overlay auto_incidents latitude and longitude data using stat_density_2d().


### INSTRUCTOR:
William Connell
PhD Student at University of California, San Francisco
