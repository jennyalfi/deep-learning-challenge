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

## Analysis: 
The purpose of this analysis is to review what parameters we used in our model and the results received.

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?
What variable(s) are the features for your model?
What variable(s) should be removed from the input data because they are neither targets nor features?
Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

## Results
First pass:
1st hidden layer nodes = 80
2nd hidden layer nodes = 30
epochs = 100
loss: 0.5550 - accuracy: 0.7254
Saved as AlphabetSoupCharity

First Optimization Attempt:
1st hidden layer nodes = 132 (increased to 3x's input)
2nd hidden layer nodes = 66
epochs = 100
loss: 0.5621 - accuracy: 0.7264 (Accuracy increased slightly)
Saved as AlphabetSoupCharity_Optimization1

Second Optimization Attempt:
1st hidden layer nodes = 132 (3x's input)
2nd hidden layer nodes = 100 (increased to 100)
epochs = 80 (reduced to 80)
loss: 0.5607 - accuracy: 0.7257
Saved as AlphabetSoupCharity_Optimization2

Third Optimization Attempt:
1st hidden layer nodes = 132 (3x's input)
2nd hidden layer nodes = 66
3rd hidden layer nodes = 33 (Added 3rd hidden layer)
epochs = 100
loss: 0.5682 - accuracy: 0.7262

