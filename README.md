## DIABETES PROJECT

## Overview
On this project, I have used the Diabetes dataset from Kaggle to predict the possibility of a patient to have a diabetes based on his/her medical records. This is a classification problem. I have used two different train methods to achieve the best score. One training method is using the hyperdrive to optimize the hyperparameters of the logistic regression model for the heart failure dataset. The second training method was the utilization of the azure automl to find the best model fit for the diabetes dataset.

Hyperdrive Model -> hyperparameter_tuning.ipynb
AutoML Model -> automl.ipynb
Finally, the best obtained model from the above two training methods is deployed using a webservice in the Azure ML studio.

## Project Set Up and Installation

This project requires access into the Azure ML studio. The following steps to be followed to initialize the project:
 
Create a new compute target in the Azure ML studio and run the above notebooks using jupyter notebooks.
Upload dataset from Github Repo that previouly download from Kaggle.

## Hyperparameter Tuning

For that training model, I used logistic regression because the task for the machine learning algorithm was to solve a classification problem. For that reason, I used the SKLEARN logistic regression model to predict the DEATH_EVENT. I tried to optimize the "C" and "max_iter" parameters of the logistic regression algorithm. The C parameter represents the inverse regularization strenght and the max_iter parameter represents the maximum number of iterations for the solvers to converge. The "C" parameter was a selection of numbers in uniform from 0.2, 0,5 to 1. For the "max_iter" parameter was a choise from the following number of iterations (25, 50, 100). I have used a random selection of these both parameters for the optimization of the logistic regression model. Finally, the banditPolicy is used as a termination policy which every two iterations checks if the primary metric which is the accuracy falls outside the top 10% range

Results
The logistic regression model achieved an accuracy of 0.78. The parameters of achieving that accuracy was "C":0.26 and "max_iter": 40 as shown in the picture below:
![](Run%20Details.png)
Screenshot of the best model is shown below:
![](best%20model.png)

Screenshot of the RunDetails is shown below:
