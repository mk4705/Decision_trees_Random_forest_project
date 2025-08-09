Loan Repayment Prediction
Project Overview
This project uses a dataset of historical loan data from LendingClub.com to predict whether a borrower will pay back their loan in full. Two different classification models, a Decision Tree and a Random Forest, are built and evaluated to determine which model performs better for this prediction task.

Exploratory Data Analysis (EDA)
Histograms were created to analyze the distribution of FICO scores, segmented by whether the loan was fully paid or not. This showed a clear trend that individuals with higher FICO scores tend to pay back their loans.

A countplot was used to visualize the number of loans for each purpose, also segmented by the not.fully.paid column.

Data Preprocessing
The purpose column, which is categorical, was converted into numerical dummy variables using one-hot encoding to be used in the models.

Model Building and Evaluation
The data was split into a training set (70%) and a testing set (30%).

Decision Tree Classifier:
A single decision tree was trained on the training data.
Predictions were made on the test set.
The model's performance was evaluated using a classification report and a confusion matrix.

Random Forest Classifier:
A Random Forest model (an ensemble of decision trees) was trained with n_estimators=600.
Predictions were made on the test set.
Performance was also evaluated using a classification report and a confusion matrix.

Results:
Both models were evaluated, but the Random Forest model performed significantly better at classifying whether a borrower would repay their loan.

Decision Tree - Although accuracy was high, it performed poorly in identifying high-risk borrowers (class 1), with a very low recall and F1-score for that class.

Random Forest - Achieved similar accuracy but showed a much better balance in precision and recall across both classes, making it a more reliable model for this task.

The Random Forest's ability to leverage multiple decision trees helps it generalize better and avoid overfitting, which is likely why it outperformed the single decision tree.
