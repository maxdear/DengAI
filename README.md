# DengAI
Machine Learning Project predicting Dengue Fever cases

# Introduction
During the UK Lockdown of Summer 2020, with the Covid-19 Pandemic at it's Peak, I, like most of the nation, was taking a greater than normal intereset in Health and Epidemiology. Having started by looking into some Covid data (which at the time was fairly limited and extremely unreliable), I came across the DengAI Driven Data competition. The task was to predict local epidemics of Dengue Fever in two South American cities; San Juan, Puerto Rico and Iquitos, Peru. Keen to excercise and increase my machine learning capabilites, I entered the tournament.

# EDA and Feature Engineering
Having looked through the data and ran some inital models, a few things became clearly necessary. Firstly, each city would have to be evaluated seperately as their locations and climates were very different. Secondly, it was clear that the time of the year was a big factor. To account for the seasonal nature of this, a 
Sin function was fitted to the cyclycal trend of weekly cases (allows for week 52 to be next to week 1). Finally, having done a little research on Mosquitos and Dengue Fever, I worked out that the relationship between ideal weather conditions (for mosquitoes) and the number of cases was delayed by 3 weeks since this was the rough incubation time for mosquitoes.

# Models and Scalers
Due to the linear nature of the data (better weather = more mosquitoes = more cases), I started testing various linear models. Having tested both a Standard Scaler and a MinMax Scaler; I chose to use a MinMax as this not only gave the best initial results but seemed to fit the data better since not all variables were normally distributed whilst the boundaries of most of them were important data points. My 4 models I chose to use were Linear Regression, Ridge Regression, Lasso Regression and also a Support Vector Regression. This last one was included becasuse I had been recently learning more about Support Vector Machines and so I was keen to put my new knowledge into practice.

# Scoring and Results
The Competition allowed 3 test data submissions per day and although I had 4 models, from some quick testing it became clear the I could drop Linear Regression as the results on the test data I had split out were clearly poorer than the other 3 models. The Scoring metric used for the results was a Mean Absolute Error rather than a more traditional R<sup>2</sup>. The reason for this was because the aim was to predict the rough trend of the cases given certain inputs rather than trying to predict the occasional week where there was a large spike. Having tested each of my models using cross validation, I was getting an MAE on the test data of roughly 5 for Iquitos and closer to 25 for San Juan. Since the average number of cases were 5 times larger in San Juan, I concluded that my models were performing equally across the two cities and hence accounting for the correct trends in climate and seasonality. My best submission score, which came from the Support Vector Regression, was an MAE of 25.29 which at the time of submitting put me in the top 1,000 submissions. Although I always belive that one can improve, I was happy with my score and also believe that any models that are scoring below 20 are likely to be overfitting.

# Conclusion
Although I did not win the competition I was happy with my effort and it was a great learning experience. It is a true, real life application of Machine Learning with an added competitive nature. For more details on the Competition please click [here](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/)


