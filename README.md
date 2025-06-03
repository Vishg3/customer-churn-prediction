# Customer Churn Prediction

This project predicts whether a customer is likely to churn based on their demographics and service usage. I used machine learning models and SHAP to make the predictions explainable.

## Problem

Churn prediction helps businesses retain customers by identifying who is likely to leave. The goal was to build an accurate and interpretable model.

## Dataset

- Dataset: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Binary classification: churn or not churn
- Note: Dataset is not included due to licensing. Download it from Kaggle and save as 'Telco-Customer-Churn.csv' in the project folder.

## Preprocessing

- Used ColumnTransformer with OrdinalEncoder and StandardScaler
- Applied SMOTE only on the training set to handle class imbalance
- Preprocessing was done inside a pipeline

## Models Tried

- Logistic Regression
- Random Forest
- XGBoost

Metrics used: accuracy, F1-score (macro and weighted), and ROC AUC.

## Final Model

The final model is a tuned XGBoost classifier:
- Accuracy: 0.779
- AUC: 0.83
- Macro F1-score: 0.72

I selected it based on its balanced performance and consistent results.

## Explainability with SHAP

SHAP was used to understand model behavior:
- Global: Contract type, tenure and monthly charges were top churn drivers
- Local: Force plots showed how features pushed individual predictions

## Prediction Function

Included a simple function to predict churn for a new customer.

## Files

- 'CustomerChurnPrediction.ipynb' – Full code and outputs
- 'xgbmodel.joblib' – Saved final model
- 'requirements.txt' – Python dependencies
- 'README.md' – Project summary

## License

MIT License
