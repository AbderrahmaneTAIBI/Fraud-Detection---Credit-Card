# Report: Random Forest Classifier for Credit Card Fraud Detection
 
## Introduction
Credit card fraud is a significant problem in the financial industry, and machine learning techniques have been widely applied to detect fraud cases. In this project, we used the Random Forest classifier to detect fraudulent transactions in a credit card dataset.

## Dataset
The dataset contains transactions made by credit cards in September 2013 by European cardholders. The dataset is highly imbalanced, with fraudulent transactions accounting for only 0.17% of the total transactions. The dataset has 284,807 rows and 31 columns, including the time, amount, and anonymized features V1-V28. It's a kaggle dataset (https://www.kaggle.com/mlg-ulb/creditcardfraud)

## Data Preprocessing
We started by loading the dataset into a pandas dataframe and exploring it using various functions like head(), tail(), describe() and info(). We noticed that the dataset had a class imbalance issue, with only 0.17% of the transactions being fraudulent. We addressed this issue by undersampling the majority class (non-fraudulent transactions). Additionally, we dropped the 'Time' column and scaled the 'Amount' column using the StandardScaler.

## Model Training and Evaluation
We split the preprocessed dataset into training and testing sets, with a test size of 0.2 and a random state of 42. We trained the Random Forest classifier on the training set and made predictions on the test set. We evaluated the performance of the model using various metrics like confusion matrix, classification report, and ROC-AUC score.

## Results
The Random Forest classifier achieved an accuracy of 0.98, which is an improvement over the Logistic Regression model we used earlier. The precision and recall for the fraudulent class (Class 1) were 0.07 and 0.84, respectively, indicating that the model correctly classified a large number of fraudulent transactions, but also had a high false positive rate. The f1-score for Class 1 was low (0.12), which is a trade-off between precision and recall.

## Conclusion
In this project, we implemented the Random Forest classifier to detect fraudulent transactions in a credit card dataset. The model achieved a high accuracy and recall for the fraudulent class, but at the expense of precision. There is a need for further improvement in the model's performance, possibly by using more sophisticated techniques like anomaly detection or neural networks.
