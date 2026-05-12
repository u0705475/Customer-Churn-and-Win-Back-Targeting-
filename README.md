# Customer Churn and Win-Back Targeting

An end-to-end churn prediction and retention decision pipeline designed for a subscription business. This project delivers calibrated churn probabilities and a budget-aware rule that managers can apply directly.

## Business Problem

Leadership requested two actionable outputs:

1. A churn probability for every active customer.
2. A simple, budget-aware rule indicating whom to contact per 1,000 customers.

This project provides a fully reproducible workflow that transforms raw customer data into calibrated predictions and a clear retention strategy.

## Approach

- Cleaned and encoded raw customer data using a reproducible preprocessing pipeline.
- Trained three models: Logistic Regression, Random Forest, and Gradient Boosted Trees.
- Evaluated all models using 5-fold cross-validation (AUC and Brier score).
- Selected a calibrated Gradient Boosted Trees model as the final model.
- Generated a reliability curve, ablation table, and out-of-fold predictions.
- Derived a manager-ready decision rule based on cost and expected value.

## Key Results

- Final Model: Calibrated Gradient Boosted Trees  
- OOF AUC: 0.846  
- OOF Brier: 0.135  
- Holdout AUC: 0.844  
- Holdout Brier: 0.136  
- Decision Rule: Contact customers with p_churn > 0.28

## Deliverables

- oof_predictions.csv  
- holdout_predictions.csv  
- figures/calibration.png  
- figures/final_calibration.png  
- Fully reproducible notebook

## Reproducibility

All preprocessing, modeling, and calibration steps are implemented inside scikit-learn pipelines to prevent leakage and ensure consistent transformations across training and holdout data.

