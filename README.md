# Predicting Prevalence of Undernourishment - DAT102x

This repository contains the Jupyter notebooks and artifacts created as part of the requirements to complete the Microsoft Professional Program Data Science capstone project. The mission was to predict Prevalence of Undernourishment from data provided by the Food and Agriculture Organization of the United Nations (FAO) and consisted of various socioeconomic statistics by country.

The FAO defines PoU as:
>An estimation of the probability that a randomly chosen individual in the population regularly consumes less food than his dietary energy required to live a healthy active life.

PoU is a statistical model and represents an estimation of how likely individuals are to suffer from chronic hunger. It is a complex metric and as such difficult to calculate, hence the desire to estimate PoU from more readily available statistics.

The notebooks are numbered in the suggested reading order, however creating them was not a linear process. There was a lot of cycles to get to these files.

For reference they are:
* 01 Data Exploration
  * Graphs and summary statistics of the data
* 02 Data Cleansing
  * Step taken to clean the data
* 03 Data Scaling and Normalising
  * Steps taken to scale and normalise the input data
* 04 Train Model
  * Train a MLPRegressor (Neural Network model)
* 05 Tune Model
  * Using Grid Search to find optimal parameters for the MLPRegressor
* 06 Explore Feature Selection
  * Trail and error various feature grouping to see if could improve the score.
* 07 Training vs Predicted Correlation Graphs
  * Graphs for the report mainly
* 08 Trend Analysis
  * Failed attempt at reverse engineering the expected results.

The final submitted report can be read in either Word .docx or Adobe Reader .pdf format. The filename is **Analysis of Chronic Hunger - DAT102x October 2018**. This report contains one major flaw:
> These features were used to train a Neural Network based prediction model. Additionally, a 4-fold stratified split was made. The stratified split was based on the country_code in order to ensure the model worked by country rather than generically.

Turned out to be simply wrong. Even though my RMSE score using this model was low enough to score a 100% mark, it turns out that **NOT** making a stratified split improved the test RMSE score by more than 25%. In the spirit of transparency I am leaving the report as it was submitted. Warts and all.

Thank you for taking the time to read this repo and feel free to come [provide feedback](https://kebnoa.com/2018/11/first-data-science-competition/) at my blog post about it.