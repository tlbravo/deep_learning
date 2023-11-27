# Neural Network Model Report

## Overview
The purpose of this analysis was to create binary classifiers that can predict whether applicants will be successful if funded by Alphabet Soup. Changing parts of the model like number of nodes, activation functions, bin numbers, etc. result in different accuracies. 

## Results

## Data Preprocessing

* The target for the model was the "IS SUCCESSFUL" column. This helps predict whether an applicate will have successful funding. 
* The features for the model were the "application_types_to_replace" and "classifications_to_replace" variables.
* The variable that was removed from the input data was the "EIN" variable. That was not beneficial to the analysis. 


## Compiling, Training, and Evaluating the Model

For my first model there were 2 hidden layers. I used the following activation functions: <br>

![nodes1](Images/nodes1.PNG) <br>

![model1](Images/model1.PNG) <br>

I noticed that the total trainable params was 619 so I thought to increase the number of params in my final model. This would hopefully increase the accuracy of the model. <br>

![results1](Images/results1.PNG) <br>

I was able to achieve an accuracy of 73% for my first model which was close to the ultimate goal of 75% accuracy. <br>


## Model Optimization

For the next model, I decided to keep the "NAME" column. I filtered out "NAME" where the value counts were less than 50. Creating more bins here could increase the number of rare occurances in the "NAME" column. 

![names2](Images/names2.PNG) <br>

This model's performance was more accurate. Increasing the number of columns that were analyzed, increaseing the hidden layers, and epochs helped raise the model's accuracy. 

![nodes2](Images/nodes2.PNG) <br>

The total number of trainable params was increased to 1535 and I increased the number of epochs to 150. 
The following activation functions were used:

![model2](Images/model2.PNG) <br>

![results2](Images/results2.PNG) <br>

The optimized model achieved an accuracy of 76%.

## Summary

Adding more bins, hidden layers, epochs increased the accuracy of the model. It took me a few attempts at reaching an accuracy of at least 75%. A more accurate model would probably be more desireable especially in industries like pharmacuticals and banking where the stakes are higher.

Another way to solve this classificatin problem would be to use ensemble learning. You can combine multiple models' (like Random Forest) to improve predicitive performance. This works by aggregating predicitons which in theory would improve accuracy and decrease overfitting. 