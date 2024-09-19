
# Model Card for Credit Card Fraud Detection Using XGBoost and SVM

## Model Overview
- **Model Type**: XGBoost (Extreme Gradient Boosting) classifier & Support Vector Machine (SVM).
- **Primary Purpose**: Detect fraudulent credit card transactions in an imbalanced dataset.
- **Version**: Final tuned versions using RandomizedSearchCV for XGBoost and GridSearchCV for SVM for hyperparameter optimization.

## Model Details (XGBoost)
- **Architecture**: XGBoost ensemble model optimized for class imbalance.
- **Key Features**:
    - Learning rate: 0.2
    - n_estimators: 300
    - max_depth: 5
    - scale_pos_weight: 1 (to handle class imbalance)
    - subsample: 1.0
    - colsample_bytree: 1.0

## Model Details (SVM)
- **Architecture**: Support Vector Machine (SVM) optimized for class imbalance.
- **Key Features**:
    - Kernel: Radial Basis Function (RBF)
    - C: 1
    - gamma: 'scale'
    - class_weight: 'balanced'

## Performance Metrics (XGBoost)
- **Precision (Fraudulent)**: 0.77
- **Recall (Fraudulent)**: 0.81
- **F1-score (Fraudulent)**: 0.79
- **ROC AUC Score**: 0.99
- **Accuracy**: 1.00 on a test set containing 56,962 transactions.
- **Confusion Matrix**:
    - True Negatives: 56,840
    - False Positives: 24
    - False Negatives: 19
    - True Positives: 79

## Performance Metrics (SVM)
- **Precision (Fraudulent)**: To be filled
- **Recall (Fraudulent)**: To be filled
- **F1-score (Fraudulent)**: To be filled
- **ROC AUC Score**: To be filled
- **Accuracy**: To be filled

## Considerations
- **Intended Use**: The models are intended for real-time fraud detection systems in credit card transactions where class imbalance is a key challenge.
- **Ethical Concerns**: Since the dataset is anonymized, no direct ethical concerns arise, but careful attention must be given to the fairness and transparency of model decisions in deployment.
- **Limitations**: The models are optimized for the specific dataset, so they may require retraining or further tuning to generalize to different datasets or environments.

## Evaluation and Maintenance
- **Ongoing Evaluation**: The models' performance should be regularly evaluated in a live environment to ensure that they continue to perform as expected with new data.
- **Updates**: Future updates to the models could include fine-tuning on new datasets or improving interpretability with SHAP values or LIME explanations.
