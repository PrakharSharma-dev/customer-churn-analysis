# Telecom Customer Churn Analysis

## The Business Problem
A telecom company is losing approximately 1 in every 4 customers 
annually — a 26.5% churn rate across 7,043 customers. Left 
unaddressed, this represents significant recurring revenue loss 
and long-term competitive decline.

## What This Project Does
This analysis identifies *who* is likely to churn, *why* they 
churn, and *what the business should do about it* — combining 
predictive modeling with actionable business recommendations.

## Key Results

| Metric | Value |
|---|---|
| Churn Rate | 26.5% |
| Model AUC | 0.848 |
| Churn Detection Rate | 81% |
| Missed Churners Reduced | 183 → 70 |
| High/Critical Customers Flagged | 605 |
| Estimated Revenue Protected | ~$111,000/year |
| Risk Tier Differential | 15.8× (Critical vs Low) |

## Project Structure

| Phase | Focus | Notebook |
|---|---|---|
| Phase 1 | Business context + data loading | 01_eda.ipynb |
| Phase 2 | Exploratory data analysis | 01_eda.ipynb |
| Phase 3 | Data cleaning + feature engineering | 02_cleaning_features.ipynb |
| Phase 4 | Modeling + SHAP interpretability | 03_modeling.ipynb |
| Phase 5 | Executive summary | reports/ |

## Top Churn Predictors (SHAP Analysis)
1. Contract type (two-year contracts = lowest churn)
2. Customer tenure (first 12 months = highest risk)
3. Internet service type (fiber optic = elevated risk)
4. Payment method (electronic check = higher churn)
5. Charge per service (engineered feature)

## Business Recommendations
1. Contract conversion for month-to-month customers
2. Structured onboarding program for first 12 months
3. Fiber optic service quality review
4. Payment method migration to auto-pay
5. Value bundling for high-risk segments

## Dashboard
Interactive dashboard built in Tableau Public.
[View Dashboard →](https://public.tableau.com/views/TelcoCustomerChurnAnalysis-RiskDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Tools Used
Python · Pandas · NumPy · XGBoost · SHAP · 
Scikit-learn · Seaborn · Matplotlib · Tableau Public

## Dataset
IBM Telco Customer Churn Dataset via Kaggle

## Author
Prakhar Sharma · BTech Computer Science ·https://www.linkedin.com/in/prakhar-sharma-dataanalyst/



---

*This project is part of an ongoing effort to build data skills with a focus on business thinking, not just technical execution.*
