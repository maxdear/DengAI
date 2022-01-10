# DengAI
Machine Learning Project predicting Dengue Fever cases

# Introduction
During the UK Lockdown of Summer 2020, with the Covid-19 Pandemic at it's Peak, I, like most of the nation, was taking a greater than normal intereset in Health and Epidemiology. Having started by looking into some Covid data (which at the time was fairly limited and extremely unreliable), I came across the DengAI Driven Data competition. The task was to predict local epidemics of Dengue Fever in two South American cities; San Juan, Puerto Rico and Iquitos, Peru. Keen to excercise and increase my machine learning capabilites, I entered the tournament.

# EDA and Feature Engineering
Having looked through the data and ran some inital models, a few things became clearly necessary. Firstly, each city would have to be evaluated seperately as their locations and climates were very different. Secondly, it was clear that the time of the year was a big factor. To account for the seasonal nature of this, a 
Sin function was fitted to the cyclycal trend of weekly cases (allows for week 52 to be next to week 1). Finally, having done a little research on Mosquitos and Dengue Fever, I worked out that the relationship between ideal weather conditions (for mosquitoes) and the number of cases was delayed by 3 weeks since this was the rough incubation time for mosquitoes.

# Models and Scalers
Due to the linear nature of the data (better weather = more mosquitoes = more cases), I started testing various linear models. Having tested both a Standard Scaler and a MinMax Scaler; I chose to use a MinMax as this not only gave the best initial results but seemed to fit the data better since not all variables were normally distributed whilst the boundaries of most of them were important data points. My 4 models I chose to use were Linear Regression, Ridge Regression, Lasso Regression and also a Support Vector Regression. This last one was included becasuse I had been recently learning more about Support Vector Machines and so I was keen to put my new knowledge into practice.

# Results
The Competition allowed 3 test data submissions per day and although I had 4 models, from some quick testing it became clear the I could drop Linear Regression as the results on the test data I had split out were clearly poorer than the other 3 models. The Scoring metric used for the results was a Mean Absolute Error rather than a more traditional R^2
