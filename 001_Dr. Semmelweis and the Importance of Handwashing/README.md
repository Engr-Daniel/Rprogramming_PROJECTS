DR. SEMMELWEIS AND THE IMPORTANCE OF HANDWASHING

Reanalyze the data behind one of the most important discoveries of modern medicine: handwashing.

MEET DR SEMMELWEIS

Hungarian physician Dr. Ignaz Semmelweis worked at the Vienna General Hospital with childbed fever patients. Childbed fever is a deadly disease affecting women who have just given birth, and in the early 1840s, as many as 10% of the women giving birth died from it at the Vienna General Hospital. Dr.Semmelweis discovered that it was the contaminated hands of the doctors delivering the babies, and on June 1st, 1847, he decreed that everyone should wash their hands, an unorthodox and controversial request; nobody in Vienna knew about bacteria.

You will reanalyze the data that made Semmelweis discover the importance of handwashing and its impact on the hospital.

Project Description
In 1847, the Hungarian physician Ignaz Semmelweis made a breakthrough discovery: he discovered handwashing and enforced it at his hospital to save hundreds of lives.
 
In this project, I reanalyze the data that made Semmelweis discover the importance of handwashing and its impact on the hospital and I answer the question how much did handwashing reduce monthly death rates on average.

This project will sharping your skills on working with tidyverse library, data manipulation and visualization.


PROJECT INSTRUCTION:
How much did handwashing reduce monthly death rates on average?

Load the CSV files into yearly and monthly data frames and check the data.
Add a proportion_deaths column to each df, calculating the proportion of deaths per number of births for each year in yearly and month in monthly.
Create two ggplot line plots: one for the yearly proportion of deaths and another for the monthly proportion of deaths. For the yearly plot, create a different colored line for each clinic.
Add a handwashing_started boolean column to monthly using June 1st, 1847 as the threshold; TRUE should mean that handwashing has started at the clinic. Plot the new df with different colored lines depending on handwashing_started.
Calculate the mean proportion of deaths before and after handwashing from the monthly data, and store the result as a 2x2 df named monthly_summary with the first column containing the handwashing_started groups and the second column having the mean proportion of deaths.
Steps Used To Approach The Project
Load and inspect the data
Add a new column with the proportions
Make a line plot for each data frame
Visualize the threshold
Calculate the mean proportion of deaths
Acknowledgement
Thanks to DataCamp and ingressive(I4G) for the scholarship provide to take this project on datacamp. 