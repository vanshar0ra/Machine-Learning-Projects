# Student Performance Prediction

## Objective
The task is to obtain the G3 scores of students based on the given set of 33 features in
the dataset.

## Approach
* The data consisted of a total of 33 features for each student and 1044 samples of
students (combining two datasets), including 3 columns for the students marks in
G1, G2, G3 and other predictive features. Task is to predict the final score in G3,
using the given features excluding G1 and G2.
* The data was split into train, test and validation sets for ensuring unbiased
evaluation of the model performance
* Redundant features were first filtered by manual screening. The numerical features
were then evaluated by taking their correlation and categorical features by dividing
the data into the various categories. The features with low correlation with the target
variable were removed. The selected categorical features were One-hot encoded.
* The models were trained on two versions of the Dataset - one with ordinary features,
second with polynomial features
* Models were evaluated on validation data using the metrics - mean absolute error
and mean squared error.
* Five kinds of models were trained and evaluated on the given data:
    - Linear Regression
    - XGB Regression
    - Polynomial Regression
    - Ridge Regression
    - Lasso Regression

## Outcome
Lasso Regression worked the best with the lowest Mean Absolute Error of approximately 2.65 marks as compared to the maximum marks of 20.

### Soure of Data:

P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance. In A. Brito and J. Teixeira Eds., Proceedings of 5th FUture BUsiness TEChnology Conference (FUBUTEC 2008) pp. 5-12, Porto, Portugal, April, 2008, EUROSIS, ISBN 978-9077381-39-7.
[Web Link](http://www3.dsi.uminho.pt/pcortez/student.pdf)
