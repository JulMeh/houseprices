# Data fun with house prices

## Introduction

In this document I am going to predict the selling price of houses. To do so, I  use data from Kaggle, do an EDA, do some transformations and finally use Advanced regression techniques to create a model for the prediction.

This project is based on the Kaggle competition "[House prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview/description)". For this reason I will also take over the general conditions of this competition:

- Competition Description: Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

- Acknowledgments: The Ames Housing dataset was compiled by Dean De Cock for use in data science education. It's an incredible alternative for data scientists looking for a modernized and expanded version of the often cited Boston Housing dataset. 

- Goal: It is your job to predict the sales price for each house. For each Id in the test set, you must predict the value of the SalePrice variable. 

- Metric: Submissions are evaluated on Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price. (Taking logs means that errors in predicting expensive houses and cheap houses will affect the result equally.)

Moreover, I try to put a focus on the use of tidyverse packages, an appealing visualization of the data and to create a readable html file. 

## Description of the procedure

1. Having read the description of the competition and the related text file, I knew from the beginning how to treat some of the NA values and the data type of each column.

2. I took a look at the histogram of the target variable and its qq plot. I also removed the remaining NA values.
![alt text](https://github.com/JulMeh/houseprices/blob/master/histoandqq.png "histoandqq")

3. I engineered some feature like:
  i. TotalBath	Total nuber of bathrooms
  ii. RemodAdd	If a house was remodeled or not
  iii. TotalSF	Size of the house in square feet above and below grade etc.

4. I took a look on the most important variables with a correlation matrix and a quick randomforst.
![alt text](https://github.com/JulMeh/houseprices/blob/master/Rf.png "Rf")

5. Nevertheless I did some preprocessing and build the lasso regression and the xgboost model.
![alt text](https://github.com/JulMeh/houseprices/blob/master/mods3.png "mods")

## Outlook
This project covers many points of a real world project. As you can tell from the work of your other projects, there is always potential for improvement:

- Try to use tidymodel to model

- Start a seconde project to go deeper into the xgboost

-  Try to optimise me code via functions and maybe a customized package
