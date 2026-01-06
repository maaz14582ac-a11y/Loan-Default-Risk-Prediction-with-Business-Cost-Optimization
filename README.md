# Loan-Default-Risk-Prediction-with-Business-Cost-Optimization
A machine learning project that predicts loan defaults and selects an optimal classification threshold using business cost optimization rather than accuracy.

## Objective
Predict loan default risk and optimize the decision threshold using a business
cost-sensitive approach rather than accuracy alone.

## Dataset
Home Credit Default Risk Dataset (Kaggle)  
File used: `application_train.csv`

Target:
- `TARGET = 1` → Loan default
- `TARGET = 0` → No default

## Approach
1. Data cleaning and preprocessing
2. Feature encoding and scaling
3. Train binary classification models
   - Logistic Regression (baseline)
   - CatBoost / RandomForest (advanced)
4. Predict default probabilities
5. Define business costs:
   - False Positive (reject good customer)
   - False Negative (approve risky customer)
6. Optimize classification threshold to minimize total business cost

## Business Cost Logic
False negatives are assigned a higher cost because loan defaults
cause greater financial loss than rejecting a safe applicant.

## Results
- Optimal threshold selected based on minimum total business cost
- Demonstrates how ML decisions align with real banking objectives

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- CatBoost (optional)
- Matplotlib
