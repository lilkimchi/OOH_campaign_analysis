# OOH Analysis

<img alt="Python" src="https://img.shields.io/badge/language-Python-blue"/>. <img alt="Jupyter" src="https://img.shields.io/badge/notebook-Google%20colab-orange"/>

### Introduction 
We are given a dataset of daily campaign data showing various mobile acquisition metrics such downloads, user registrations, activations, and tours. The time period takes place over an approximate 65 day period and it includes daily time series data from before the insertion of the campaign until after its end.

I used Python and Pandas to clean and explore the data, along with Google's R package CausalEffect running in a python environment. 

### Question
What was the impact of our offline campaign? In a digital world of tracking cookies and clicks, measuring the impact of hard-to-measure marketing efforts can be a challenging task. 

We can use causal inference to understand the effects and determine the effect of the insertion of the campaign and whether it impacted acquisition KPIs. We can fit a model using Bayesian structural time series to make predictions on how acquisition metrics would have performed had the intervention of the TV campaign not taken place. 

Data is divided into 2 parts: the period before the campaign (pre-period) and the period after the campaign start (post-period). 

### Performance over time
<img src='OOH_images/Performance.png' width=700>

### Difference between the actual series and the predicted series
<img src='OOH_images/pointwise.png' width=600>

### Cumulative effect, showing the summation of the point effects accumulated over time
<img src='OOH_images/cumulative.png' width=600>

### Results
The model and report confirm that the cause for the lift in downloads was the introduction of the TV campaign.
<img src='OOH_images/download_summary.png' width=600>


It had an effect of 3598 new downloads with a 95% confidence interval. The p-values less than 0 tell us the results are statistically significant and unlikely due to random chance.






