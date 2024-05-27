# WHAT IS YOUR HEART RATE TELLING YOU?

Examine the relationship between heart rate and heart disease using multiple logistic regression.


## Project Description
Heart disease is the leading cause of death in the USA. This project uses the Cleveland heart disease dataset to examine the relationship between the maximum heart rate one can achieve during exercise and the likelihood of developing heart disease. Using multiple logistic regression, you will handle the confounding effects of age and gender.


## Project Instructions
Assess the maximum heart rate one can achieve during exercise and how it is associated with a higher likelihood of getting heart disease by answering the following questions:

- Manipulate the data and use statistical tests to see which predictors are related to heart disease as indicated by the `class` column.
	- Adjust the `class` column to be binary where `0` indicates no heart disease and `1` represents the presence of heart disease.
	- Save the three features with the highest significance to a list called `highly_significant`.

- Fit a model using your highly significant features to predict the likelihood of heart disease, adjusting the results to be a binary outcome for probabilities greater than 0.5.

- Calculate and save the following model metrics: accuracy as a numeric variable `accuracy`, and the confusion matrix as `confusion`.

**How to approach the Project**
1. Find the significant variables

2. Fit a model to predict the probability of heart disease

3. Calculate the model metrics

## Instructor:
Jasmin Ludolf

Data Science Content Developer, DataCamp