# deep-learning-challenge
Module 21 Challenge

## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Data Source
https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv

## Instructions
### Step 1: Preprocess the Data

### Step 2: Compile, Train, and Evaluate the Model

### Step 3: Optimize the Model

## Analysis Overview: 
The purpose of this project was to use a neural network deep learning model with our dataset to see how well this model can predict successful applicants. 

## Results: 

### Data Preprocessing

Our y variable and target for this model is the IS_SUCCESSFUL column.

Our X variables and features for this model are:
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

The identification variables, EIN and NAME, were removed from the input data because they are neither targets nor features.

### Compiling, Training, and Evaluating the Model

The reLU activation function was selected for the first hidden layer since this is most effective for positive nonlinear input data for classification. I used Sigmoid activation for the output layer since we are performing a binary classification. I followed the general rule of using 2-3 times as many neurons as there are input features. I started with 100 epochs and did not increase as I could see that the later epochs didn't improve model accuracy.

First pass:
* 1st hidden layer neurons = 80
* 2nd hidden layer neurons = 30
* epochs = 100
* accuracy: 0.7254

First Optimization Attempt:
* 1st hidden layer neurons = 132 (increased to 3x's input)
* 2nd hidden layer neurons = 66 (increased to 66, half of first layer)
* epochs = 100
* accuracy: 0.7264 (Accuracy increased slightly)

Second Optimization Attempt:
* 1st hidden layer neurons = 132 (3x's input)
* 2nd hidden layer neurons = 100 (increased to 100)
* epochs = 80 (reduced from initial 100)
* accuracy: 0.7257

Third Optimization Attempt:
* 1st hidden layer neurons = 132 (3x's input)
* 2nd hidden layer neurons = 66
* 3rd hidden layer neurons = 33 (Added 3rd hidden layer)
* epochs = 100
* accuracy: 0.7262


I did not achieve higher than 75% accuracy for this model after several attempts and the accuracy changed little regardless of the changes made. I tried changing the binning for rare occurances and adjusted the hyperparameters, such as adding neurons, adding another hidden layer, and reducing the epochs. 

## Summary: 
This binary classification neural network machine learning model was designed to help predict which applicants have the best chance of success. The goal was to try to achieve accuracy above 75%, but this was not attained after several optimization attempts. Each attempt made little difference in the accuracy of the model. The highest accuracy I attained was on the first optimization attempt with 72.64% accuracy. To improve this deep learning model we could try performing additional preprocessing of the data to see if that helps to improve accuracy. We could also try a regression model like Random Forest which is good for nonlinear data and is capable of both regression and classification.


