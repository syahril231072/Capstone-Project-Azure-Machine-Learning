## Hyperparameter Tuning

For that training model, I used logistic regression because the task for the machine learning algorithm was to solve a classification problem. For that reason, I used the SKLEARN logistic regression model to predict the DEATH_EVENT. I tried to optimize the "C" and "max_iter" parameters of the logistic regression algorithm. The C parameter represents the inverse regularization strenght and the max_iter parameter represents the maximum number of iterations for the solvers to converge. The "C" parameter was a selection of numbers in uniform from 0.1 to 1. For the "max_iter" parameter was a choise from the following number of iterations (5, 10, 20, 40, 50, 80, 100, 150, 200). I have used a random selection of these both parameters for the optimization of the logistic regression model. Finally, the banditPolicy is used as a termination policy which every two iterations checks if the primary metric which is the accuracy falls outside the top 10% range

Results
The logistic regression model achieved an accuracy of 0.78. The parameters of achieving that accuracy was "C":0.26 and "max_iter": 40 as shown in the picture below:
![](Run%20Details.png)
Screenshot of the best model is shown below:
![](best%20model.png)

Screenshot of the RunDetails is shown below:
