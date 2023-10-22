# Housing_Ridge_Lasso_Assignment

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## General Information
### Problem Statement:
The company wants to know:

Which variables are significant in predicting the price of a house, and
How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.

### Business Goal:
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

### Technical Goal:
determine the optimal value of lambda for ridge and lasso regression.

## Disclaimer:
1.To execute the code, train.csv (data file) should be in the same location.
2.Target value is normalized using MinMaxScaling

## Technologies Used

Models are implemented using the python language.
### Imported libracies 
import numpy as np
import pandas as pd
import missingno as msno
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn import linear_model, metrics
from sklearn.linear_model import LinearRegression, Ridge, Lasso
from sklearn.preprocessing import PolynomialFeatures, MinMaxScaler
from sklearn.model_selection import GridSearchCV
from sklearn.metrics import mean_squared_error, r2_score

import os


## Conclusions

### RIDGE REGRESSION MODEL:
Ridge Regression Model : choose lambda - 0.001

Lamda:0.001

    Training Data:
        r2score: 0.8625557120840566
        RMSE:0.040699754348539785

    Testing Data:
        r2score: 0.8592177853257507
        RMSE:0.04179933989310499
        
    Top 5 predictor variables:
      1stFlrSF      :0.34028563
      LotArea       :0.17233748
      2ndFlrSF      :0.14791761
      age           :-0.11999162
      OverallCond_9 :0.1192196
        
### LASSO REGRESSION MODEL:
Lasso Regression Model: choose lambda = 0.001 - some more coeff values are zero

Lamda:0.001

    Training Data:
        r2score: 0.8051467736454287
        RMSE :0.048459869554225314

    Testing Data:
        r2score: 0.7958201652667687
        RMSE :0.05033869480512303
    
    Top 5 predictor variables:
        1stFlrSF      :0.253522
        2ndFlrSF      :0.113366
        OverallQual_10:0.097391
        OverallQual_9 :0.094984
        age           :-0.078841

## Contact
Created by [@MChethana] / Chethana Manyam- feel free to contact me!
        
