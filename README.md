# Neural Network Charity Analysis

## Overview

Alphabet Soup, a nonprofit foundation, is a philanthropic foundation dedicated to helping organizations that protect the environment, improve people's well-being, and unify the world. Alphabet Soup has raised over $10 billion in the past 20 years and have used that money to invest in lifesaving technologies and organize reforestation groups around the world. 

With our knowledge of machine learning and neural networks, we used the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

The goal of this analysis was to develop a model with over 75% accuracy in predicting success from the dataset. To do this, we used Pandas, Scikit-learn, and Tensorflow. 

## Results

### Data Preprocessing

I. Variable considered the target for our model:

The target variable for our model was the *IS_SUCCESSFUL* column
   
II. Variables considered the features for our model:

All columns other than the *EIN* and *NAME* columns were considered features for our model. 

III. Variable considered neither targets nor features, and removed from the input data:

The *SPECIAL_CONSIDERATIONS_N* column was dropped as it was redundant to the *SPECIAL_CONSIDERATIONS_Y column. 

### Compiling, Training, and Evaluating the Model

I. Number of neurons, layers, and activation functions selected for our neural network model:

The first model had two hidden layers, the first with 80 neurons and the second with 45 neurons. Both hidden layers used the relu activation function while the output layer used the sigmoid activation function. 

II. Target model performance:

With our initial setup, an accuracy score of roughly 72.5% was achieved. Therefore, we failed to achieve the target model performance of over 75%.

III. Steps taken to try and increase model performance:

In order to increase model performance, the following steps were taken:
     
* Binned INCOME_AMT values greater than $5 million into a '5M+' bin
* An additional hidden layer was added with 40 neurons
* The activation function for the three hidden layers were changed from relu to tanh
* The training epochs increased from 100 to 150, and up to 200
* The number of Neurons in each hidden layer increased slightly

## Summary

The results of our optimizations unfortunately did not yield the ideal results. For future attempts, it may be beneficial to attemp other methods such as random forest or SVM. This, along with plenty of experimentation with the dataset and model features, could potentially result in an accuracy of over 75%.
