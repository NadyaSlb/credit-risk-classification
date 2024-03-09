# credit-risk-classification

## Analysis

* The purpose of the analysis is to predict a binary outcome.
* I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
* I was trying to predict variable 'loan_status'. A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* The stages of the machine learning process I went through are read the `lending_data.csv` data into a Pandas DataFrame, create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns, split the data into training and testing datasets by using `train_test_split`, fit a logistic regression model by using the training data (`X_train` and `y_train`), save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model, calculate the accuracy score of the model, generate a confusion matrix, and print the classification report.
*  "LogisticRegression" in scikit-learn is a machine learning tool that provides a simple and effective way to build and evaluate predictive models for binary classification tasks.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* The balanced accuracy score is 0.9442676901753825. It indicates that the model performs well in correctly predicting instances from both classes(class "0" and class "1")

* Precision is the ratio of correctly predicted positive observations to the total predicted positives. For class 0, precision is 1.00, indicating that all predictions for class 0 were correct. For class 1, precision is 0.87, indicating that 87% of the predictions for class 1 were correct.

*  Recall is the ratio of correctly predicted positive observations to the all observations in actual class. For class 0, recall is 1.00, indicating that all actual class 0 instances were correctly predicted. For class 1, recall is 0.89, indicating that 89% of the actual class 1 instances were correctly predicted.

## Summary

* The model performed very well, with high accuracy, precision, recall, and F1-score, indicating its effectiveness in classifying loans. I would recommend the model for use by the company.
* In this dataset we have one class is much more prevalent than the other (we have 75036 instances of "0" and 2500 of "1"). A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting. So correctly predicting the minority class (1's) might be more critical. Misclassifying a high-risk loan as healthy (a false negative) could have significant financial implications for the lender, as they may extend credit to a borrower who is likely to default. But misclassifying a healthy loan as high-risk (a false positive) might result in some inconvenience for the borrower but is generally less damaging to the lender.

