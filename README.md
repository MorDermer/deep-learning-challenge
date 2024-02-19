# deep-learning-challenge
Homework#21

# Final Analysis and Report

The purpose of the model was to create an algorithm to help Alphabet Soup, predict whether or not applicants for funding will be successful. The model was a binary classifier that was able to predict with a fairly high degree of accuracy if the funding will be successful or not.


1) What variable(s) are the target(s) for your model?
The variable for the Target was identified as the column IS_SUCCESSFUL.


2) What variable(s) are the features for your model?
The following columns were considered as features for the model:
NAME
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE
ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT


3) What variable(s) should be removed from the input data because they are neither targets nor features?
The column or variable that can be removed is EIN as it is an identifier for the applicant organization and has no impact on the behavior of the model.


4) How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the Optimized version of the model, I used 3 hidden layers each with multiple neurons which increased the accuracy to <73% to 78%. The Initial model had only 2 layers. Although the number of epochs did not change between the Initial and the Optimized Model, adding a 3rd Layer increased the accuracy of the model.


5) Were you able to achieve the target model performance?
Yes by optimizing the model, I was able to increase the accuracy from 73% a over 78%.

6) What steps did you take in your attempts to increase model performance?
- The following steps were taken to optimize and increase the performance of the model:
Instead of dropping both the EIN and Name columns, only the EIN column was dropped. However, only the names which appeared more than 5 times were considered.
- Added a 3rd Activation Layer to the model in the following order to boost the accuracy to > 75% :

1st Layer - relu
2nd Layer - tanh
3rd Layer - sigmoid

Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

Summary and Recommendation

Overall, by optimizing the model we are able to increase the accuracy to above 78%.
This means we are able to correctly classify each of the points in the test data 78% of the time. In other words an applicant has a close to 80% chance of being successful if they have the following:

The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
The type of APPLICATION is one of the following: T3, T4, T5, T6 and T19
The application has the following values for CLASSIFICATION: C1000, C1200, C2000,C2100 and C3000.

Alternative Method
Although this model worked very well and provided a great deal of accuracy, an alternative approach to recommend is the Random Forest model as it is also suited for classification problems. Using the Random Forest model we can achieve close to 78% accuracy.
