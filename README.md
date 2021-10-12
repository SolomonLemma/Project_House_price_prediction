# Project: Ames Housing  Price Prediction

This is the second project of Data Science Immersive course in General Assembly's submitted by July 2021.

The **Ames Housing Price Analysis** data was used to come up with a prediction model for house sales. The project defined the problem of the statement, 
explore the data, perform EDA, clean the data, engineered the features based on their distribution, and made a possible prediction on the property sale prices 
using Multilinear Regression models together with Lasso and Ridge regularization.


### Overview

In the current housing market, so many factors affect the price trend most importantly rooms numbers, size, location of the house, built years, and 
construction materials are among the top list. The property prices can highly fluctuate with economic conditions, housing demand in the region, pandemic
(like covid 19 cases), government tax, and regulations, mortgage rates, neighborhood infrastructures development, etc 
(sources: https://www.noradarealestate.com/blog/housing-market-predictions/.  However, it can be possible to predict the trend of the house sales price 
with the collected property features over certain times and regions to help real estate businesses and consulting house buyers for their optimal benefit. 
The most important features of the house in Ames city in Iowa were employed for fair prices prediction from the given features for the use of real estate 
agents and the buyers.


### Problem Statement


The project aimed to make a prediction model to get the optimal house sale price with a corresponding Id at a better accuracy level that can help businesses 
for their decision. In addition, the work addressed how certain house's features are important to determine the sale price over the others.


## Executive Summary

The data were explored to understand the data types and handling the missing data. EDA was employed to visualize the missing values, the categorical 
representation of the values, and identifying outliers. The missing values were substituted based on how many values missed in a given feature to make 
a sensible consideration on removing over replacing the missed values and the outliers. The data features were classified into numerical and categorical 
types. 

The cleaned categorical variables were used dummy coding to make dummy variables on selected features to utilize in train test split data for the effective 
model. Subsequently, cross-validation was used with the train and test scores to compare with each other. Meanwhile, the model was evaluated with establishing 
fit linear regression and used regularization of Lasso/ Ridge towards improving the model for the actual prediction model. The predicted results of the 
houses prices in Ames, IA with the corresponding Id uploaded to kaggle computation. At last, the results observations and practical recommendations are 
listed out at the end to address the project objective.


### Data Description


This project used the Ames Housing data to predict the house sale prices.  The data is provided from the kaggle competition webpage (https://www.kaggle.com/c/dsi-ames/data). The files contain three files:

- `train.csv`: consist of all the features including the target, _SalePrice_. This was explored, cleaned, and hold selected features that used to train 
the models.

-  `test.csv`: contains all the features except the target, _SalePrice_. This value used for model evaluation and submissions to kaggle.

- `sample_sub_reg.csv`: a sample file for the kaggle submission format. Contains only the _Id_ & predicted _SalePrice_.

In general, the provided data comprised features that can affect the interest of house buyers and sellers for price determination. For instance, 
room sizes, number of rooms, footage of the lot, built year, locality, quality of the house, and amenities that are included in the provided dataset.



### Models and Evaluation

The Project used the following models and evaluation methods:
- Multiple Linear Regression: Using multiple explanatory features to train the model
- Lasso Regression: Using penalty term $\alpha$ to perform regularization
- Ridge Regression: Using penalty term $\alpha$ to perform regularization

The linear regression evaluation were investigated with $R^2$, and $MSE$ or $RMSE$ to determine the closeness of predicted target values with the true target values ($R^2$) and  the error values between the predicted and true target values.


### Outlines of the Contents

These are the contents of the project:

- [1 Load the Dataset](#1-Load-the-Data)
 * [1.1 Importing Libraries](#1.1-Import-the-libraries)
 * [1.2 Reading the Data](#1.2-Reading-the-Data)
 * [1.3 Assessing and Dealing with Missing Values](#1.3-Assessing-and-Dealing-with-Missing-Values)
- [2 EDA and Train Data Cleaning](#2-EDA-and-Train-Data-Cleaning)
 * [2.1 Identify Missed Values](#2.1-Identify-Missed-Values)
 * [2.2 Imputing  the Train Columns](#2.2-Imputing-the-Train-Columns)
 * [2.3 Examine Numeric Features](#2.3-Examine-Numeric-Features)
 * [2.4 Data Type Validation](#2.4-Data-Type-Validation)
- [3 Loading and Preprocessing Test Data](#3-Loading-and-Preprocessing-Test-Data)
- [4 Model Productions for Predicting the Sale Price](#4-Model-Productions-for-Predicting-the-Sale-Price)
 * [4.1 Multiple Linear Regression](#4.1-Multiple-Linear-Regression)
 * [4.2 Lasso Regression](#4.2-Lasso-Regression)
 * [4.3 Ridge and Lasso Regression](#4.2-Ridge-and-Lasso-Regression)
- [5 Prediction](#5-Prediction)
- [6 Conclusions and Recommendations](#6-Conclusions-and-Recommendations)


The train and test data were fully cleaned and scaled before model evaluation. 


The following figures indicated the cleaning and EDA before and after cleaning of the dataset


![](./images/Train_data_before_cleaning.png)
Figure 1: Shows the train data before cleaning


![](./images/Cleaned_train_dataset.png) 
Figure 2: Train data after cleaned all the missed values.



![](./images/Test-data-prior-to-cleaning.png)     
Figure 3: It is the visaulization of the test data before cleaning 


![](./images/Cleaned-Test-data.png) 
Figure 4: The test data after fully cleaned.


![](./images/True-vs-pred.png)
Figure 5: Visualization of True value vs predicted values of sale price.


6 Conclusions and Recommendations

The project dealt with housing data from the city of Ames, Iowa which consists of the detailed properties for sales in the years 206 to 2010.  The original 
data contains 81 features including the target, a large share of the data have missing values that are not used by the regression models. Some features were 
combined to make one column after significantly studied their similarity to each other.  At last, $208$ significant features including the dummified one 
were selected and cleaned for the models.  A great deal of data exploration features engineering based on reasonable correlate with the target, visualization(
whenever necessary), including scaling was carried out to develop models that can be used for predicting the sale prices. In the validation of the train 
data obtained RMSE values of $\$30199$ and $\$22143$ values for the train and test data.</p>

The model was applied and evaluated their performance both using Lasso and Ridge regularization regression to find the best and optimal prediction with a 
base price of $\$181469$. The mean coefficient values in the unit price increment in the feature value raise with house price by its respective coefficient 
value obtained with ridge modeling. The general zoning classification of the sale,  neighborhood, exterior covering, sale type, and proximity to the main 
road or railroad are among the top-five list of the coefficients obtained from the model prediction. The analysis recommended these features are the most 
significant to the seller to improve the rate of getting better values for the real estate.  On the contrary, the analysis revealed the properties with 
OldTown neighborhood, low Kitchen quality, under utilities (No Sewer, no Electricity, no Gas, and no Water (Septic Tank), mansard roof, and poor basement 
quality (height <70 inches) features have low effect on the determination of the selling price.  Finally, the sale price prediction was performed with 
r2 values of about 90% and better evaluation values to performance prediction. The obtained prediction values as a single file submitted in the of 
kaggle Ames Housing Price.
