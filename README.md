# Neural Network Charity Analysis

## Overview of the analysis
The purpose of this analysis is to use a neural network to decide which companies should receive loans from Alphabet Soup, this analysis uses python's TensorFlow library to create, train, and evaluate data gathered from previous loans. We should employ statistics and machine learning to help test and optimize the models. We strive to create a robust *deep learning neural network algorithm* that is capable of interpreting large complex datasets. This model will help Alphabet Soup determine which organizations should receive donations.

In this undertaking we need to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

## Results

### Data Preprocessing
* What variable(s) are considered the target(s) for your model?

    The "IS_SUCCESSFUL" is the target or dependent variable which we will use to train the model.

* What variable(s) are considered to be the features for your model?

    The independent variables, all the variables except the target variable, are considered the feature variables. We may remove variables like EIN     and NAME that are Identification columns and are not involved in the model.

* What variable(s) are neither targets nor features, and should be removed from the input data?

    Variables that did not classify as features or target (EIN and NAME) were removed. Moreover, variables with unique values and outliers were also    taken care of (bucketing).

### Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

    The number of neurons and layers, especially  hidden layers, could increase the efficiency to certain extents and beyond a certain point they would not add too much value. Accordingly, a low to moderate number of neurons were considered for the model to reduce superfluous computational processing and time (Please see below).


#### ***Initial results without optimization***

Two hidden layers, with respectively 80 and 30 neurons, were used. 

For the 1st and 2nd hidden layers Relu and for the output layer Sigmoid activation functions were used, respectively.

The model rendered an accuracy rate of about 72% and a loss of 56 (Figure 1).

***Loss*** is the quantitative measure of deviation or difference between the predicted output and the actual output in anticipation. It gives us the measure of mistakes made by the network in predicting the output (1).

#### Figure 1: Results without optimization

--------------------
![resultsWithoutOptimization](/pics/resultsWithoutOptimization.PNG)
---------------------

#### ***Results upon three attempts and optimization*** 

Two hidden layers, with respectively 20 and 15 neurons, were used. 

For the 1st and 2nd hidden layers Relu and for the output layer Sigmoid activation functions were used, respectively.

The model was able to reach the target value by 76% of accuracy after three attempts and optimization (Figure 2).

#### Figure 2: Results after three attempts and optimization

--------------------
![resultsAfterThreeAttemptsAndOptimization](/pics/resultsAfterThreeAttemptsAndOptimization.PNG)
---------------------

## Summary 

Initially, the model had an accuracy rate of 72% and a loss score of 55%. Upon Optimization the model's accuracy rate improved to 76% and met the target value and the loss decreased to 48%. 

Given the low accuracy of the model, it could be applicable to preliminary screening of the applications. 

On the improvement of the model, use of a ***Random Forest Classifier*** might be a good option to consider as there are a noticeable number of variables or features. Moreover, addition of more data is always a great help.
