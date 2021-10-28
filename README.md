# Neural_Network_Charity_Analysis

## Overview

The purpose of this project is to use a neural network to decide which companies should recieve funding from Alphabet Soup. 

For this analysis will be used python's TensorFlow library to create, train, and evaluate data gathered from previous loans.

## Results

### Data Preprocessing

- The target variable is the "IS_SUCCESSFUL" column 
- Non beneficial columns such as "EIN" and "NAME" were removed 
- The remaining columns became the features for the model

### Compiling, Training, and Evaluating the Model

#### First Attempt

The first attempt at compiling a neuron network consisted of: 
- 80 neurons in the first layer and 30 in the second, all 2 layers had relu activation functions and the output layer had sigmoid activation function. These parameters were selected as relu is a better fit for nonlinear data, and with two layers the model allows the second layer to reweight the inputs from the first layer. 
- The model was unable to achieve 75% accuracy.
- In an attempt to increase the model performance 3 more steps were tried as described below.

![First](https://github.com/carolineshipley/Neural_Network_Charity_Analysis/blob/main/Resources/AlphabetSoup.PNG)

#### Second Attempt

On the second attempt the columns "SPECIAL_CONSIDERATIONS" and "STATUS" were removed was was thought that it could also be non beneficial for the model. The threshold for the classification column was lowered in an attempt to have more unique values. It was kept two layers with 100 and 50 neutrons in each. The preformance metrics of this model are shown below.

![V1](https://github.com/carolineshipley/Neural_Network_Charity_Analysis/blob/main/Resources/Optimized_V2.PNG)

#### Third Attempt

On the third attempt the column "STATUS" was re-added because when was removed the accuracy of the model went down. It was kept two layers with 100 and 50 neutrons in each. The preformance metrics of this model are shown below.

![V2](https://github.com/carolineshipley/Neural_Network_Charity_Analysis/blob/main/Resources/Optimized_V1.PNG)

#### Fourth Attempt

On the fourth attempt it was kept two layers with 120 and 60 neutrons in each. The preformance metrics of this model are shown below.

![V3](https://github.com/carolineshipley/Neural_Network_Charity_Analysis/blob/main/Resources/Optimized_V3.PNG)

## Summary

The conlusion of this analysis is that after four attempts the model was unable to achieve an accuracy rating of 75%. 

A recommendation to further improve accuracy is to consider an application which can put X & Y variables through a variety of standard models with base / default parameter selection and the result output would compare accuracy for each model.
