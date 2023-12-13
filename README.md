# StarbucksCapstoneChallenge
## Installation
There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Overview
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that is the challenge to solve with this data set.

## Problem Statement
There are three main datasets to use for further analysis and processing:
* portfolio.json — containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json — demographic data for each customer
* transcript.json — records for transactions, offers received, offers viewed, and offers completed

Our main objective is to perform exploratory data analysis in these three main datasets and perform different visualizations based on transaction, demographic and offer data. Perform needed data cleaning techniques in order to prepare these datasets for the final process which is building a ML model in order to predict how much the customers will spend when performing a transaction from the offer.

## Metrics
Selecting appropriate evaluation metrics is crucial when assessing the performance of a machine learning model, especially for regression tasks involving continuous variables. In my case where I am trying to predict how much a customer will spend based on transaction and demographics data, choosing R-squared (R2 score), Mean Absolute Error (MAE), and Mean Squared Error (MSE) demonstrates a comprehensive approach to model evaluation.

## Implementation
In this section, I will define X and y variables from the cleaned dataset.As our target is to predict amount spent from customers then the y variable will be ‘amount_spent’ column and all the other columns ‘time’, ’age’, ’income’, ’Year’, ’Month’, ’Day’, ’Transaction_frequency’, ’IncomeAgeRatio’, ’IsSummer’,’ AmountPerTransaction’ will be X variable.Then we split both datasets into train and test. I will be using four types of ML models in order to evaluate them based on metrics I mentioned above: r2_score, mse and mae.

## Reflection
From the given datasets portfolio, profile and transcript, when performing EDA for each of the dataset I can say that portfolio is well organized with no missing data and really clear and concise but it could not be used in my final dataframe because in records of type transaction there are no offer id on which offer the customer has spent.

While the two other datasets had missing values, we had to impute values for missing data on each profile and transcript datasets. And in the end I had to recreate features for my final dataframe in order to have a better result for my predictions.

## Improvements
An improvement could be having the offer id on our transcript dataframe for records of type transaction in order to play with the portfolio details also in our ML models.
Also we can consider adding more features, exploring other models, handle better the categorical features and maybe address missing data in better ways.

## Motivation
I have completed this project as a part of the Udacity Data Science Nanodegree Program - Starbucks Capstone Challenge.

## Medium Blog
(https://medium.com/@subashiklajbi/starbucks-capstone-challenge-f762f4b8d49b)
