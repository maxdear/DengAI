# DengAI
Machine Learning Project predicting Dengue Fever cases

# Introduction
During the UK Lockdown of Summer 2020, with the Covid-19 Pandemic at it's Peak, I, like most of the nation, was taking a greater than normal intereset in Health and Epidemiology. Having started by looking into some Covid data (which at the time was fairly limited and extremely unreliable), I came across the DengAI Driven Data competition. The task was to predict local epidemics of Dengue Fever in two South American cities; San Juan, Puerto Rico and Iquitos, Peru. Keen to excercise and increase my machine learning capabilites, I entered the tournament.

# EDA and Feature Engineering
Having looked through the data and ran some inital models, a few things became clearly necessary. Firstly, each city would have to be evaluated seperately as their locations and climates were very different. Secondly, it was clear that the time of the year was a big factor to account for and so a Sin function was used to capture this cyclycal nature. Finally, having done a little research on Mosquitos and Dengue Fever, I worked out that ideal weather conditions for mosquitos to breed would increase the number of cases after 3 weeks since this was the rough incubation time for mosquitoes.

