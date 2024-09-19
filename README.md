# Credit-Card-Fraud
Credit Card Fraud detection 
Card Fraud Detection
Jupyter Notebook with code, experimentation, further insights, and deployment 


Business Goal
Credit card fraud is a significant issue faced by financial institutions globally, leading to billions of dollars in losses annually. The objective of this analysis is to develop machine learning models to identify fraudulent transactions in real-time, ensuring enhanced security and reducing financial losses. Early detection of fraudulent activities can help companies protect both customers and their assets, creating a safer digital environment for transactions.

Data "https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data"
The dataset used in this project is sourced from Kaggle and contains transactions made by European cardholders in September 2013. This dataset presents a significant class imbalance, where fraudulent transactions are only 0.172% of the total. It consists of 284,807 transactions, with 492 classified as fraudulent.
More info on this dataset: Kaggle Credit Card Fraud Detection Dataset.
The dataset contains the following key features:
•	V1-V28: Principal components obtained through PCA (due to privacy concerns, original features are not provided).
•	Time: Number of seconds elapsed between this transaction and the first transaction.
•	Amount: Transaction amount.
•	Class: Label, where 1 represents fraud and 0 represents non-fraud.

Modeling and Performance

In this project, various machine learning models were employed to classify transactions as fraudulent or non-fraudulent. The models tested include:
•	Logistic Regression
•	Random Forest
•	XGBoost (Extreme Gradient Boosting)
•	AdaBoost
•	Support Vector Machine (SVM)


Each model was trained and evaluated using a train/test split, with subsequent performance improvements using hyperparameter tuning (via GridSearchCV) and cross-validation to enhance accuracy.
Results:
•	Best Model: XGBoost
After hyperparameter tuning, the XGBoost model achieved the best performance:
o	Precision (Fraud): 0.77
o	Recall (Fraud): 0.81
o	ROC AUC Score: 0.987
o	Confusion Matrix:
	False Negatives: 19
	False Positives: 24
These metrics indicate that the XGBoost model offers a good balance between precision and recall, effectively identifying fraudulent transactions while minimizing false positives.

Conclusions
The analysis reveals that certain features significantly impact the model’s ability to identify fraud. Specifically:
•	Transactions with unusually high amounts are positively correlated with fraud.
•	Some principal components from PCA contribute heavily to fraud detection, indicating specific transaction patterns common to fraudulent behavior.
The XGBoost model stood out for its superior performance, making it the preferred model for this fraud detection task.
Actionable Insights
Based on this analysis, several actions can be taken to mitigate the risk of fraud:
•	Transaction Monitoring: Implement real-time transaction monitoring systems using the XGBoost model to flag potentially fraudulent activities.
•	Customer Alerts: Automate alerts to customers for suspicious transactions and provide easy mechanisms to dispute fraudulent charges.
•	Further Model Improvements: Continue to collect more transaction data to enhance the model’s ability to detect new fraud patterns.
Next Steps
Future work includes deploying this model into production, where it can be integrated with banking systems for real-time fraud detection. Ensemble techniques and neural networks can also be explored to improve detection rates further.

