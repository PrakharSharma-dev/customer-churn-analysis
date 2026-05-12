# Customer Churn Analysis — Telecom Industry

> Predicting and understanding customer churn using machine learning and business-driven analysis on the IBM Telco Customer Churn dataset.

---

## Business Objective

Customer churn is one of the most critical challenges in the telecom industry. Acquiring a new customer costs 5–10x more than retaining an existing one. This project identifies **which customers are at risk of churning, why they churn, and what actions can reduce it** — translating raw data into actionable business strategy.

---

##  Project Structure

```
customer-churn-analysis/
│
├── data/
│   ├── raw/                    # Original IBM Telco dataset (unmodified)
│   └── processed/              # Cleaned, encoded, and split data (model-ready)
│
├── notebooks/
│   ├── phase1_business_understanding.ipynb
│   ├── phase2_exploratory_data_analysis.ipynb
│   ├── phase3_data_cleaning_feature_engineering.ipynb
│   └── phase4_modeling.ipynb   # (in progress)
│
├── visuals/                    # All saved EDA and model charts
├── reports/                    # Business insights and summary reports
├── dashboard/                  # Tableau / Power BI dashboard files
└── README.md
```

---

##  Dataset

- **Source:** [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 customers × 21 features
- **Target Variable:** `Churn` (Yes / No)
- **Churn Rate:** ~26.5%

---

## 🔍 Project Phases

### ✅ Phase 1 — Business Understanding
- Defined the business problem and success metrics
- Established context: what churn costs, why it matters, what questions to answer

### ✅ Phase 2 — Exploratory Data Analysis
- Analyzed churn across demographics, contract types, services, and charges
- **Key findings:**
  - First 12 months represent the highest churn risk window
  - Month-to-month contracts churn at 3x the rate of two-year contracts
  - Senior citizens, electronic check payers, and fiber optic users are high-risk segments
  - Tenure is the strongest numeric predictor of churn
  - Long-term customers (36+ months) show dramatically lower churn rates

### ✅ Phase 3 — Data Cleaning & Feature Engineering
- Fixed data types and handled 11 missing values in `TotalCharges`
- Encoded binary columns (Label Encoding) and multi-category columns (One-Hot Encoding)
- Engineered 3 business-driven features:
  - `tenure_group` — captures lifecycle churn risk (New / Developing / Loyal)
  - `num_services` — proxies customer switching cost and stickiness
  - `charge_per_service` — flags potential value dissatisfaction
- Applied stratified 80/20 train-test split (churn rate preserved at 26.54% in both sets)
- Standardized numeric features using StandardScaler (fitted on train only — no data leakage)
- **Final model-ready dataset: 7,043 rows × 34 features**

### 🔄 Phase 4 — Predictive Modeling *(in progress)*
- XGBoost classifier for churn prediction
- SHAP values for model interpretability and business explainability

### ⏳ Phase 5 — Business Insights Synthesis
### ⏳ Phase 6 — Dashboard & Portfolio Packaging

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Explainability | SHAP |
| Dashboard | Tableau / Power BI |
| Environment | Google Colab, GitHub |

---

## 💡 Key Design Principles

- **Business questions drive every section** — each notebook section starts with the problem, not the code
- **No data leakage** — scaler fitted on training data only
- **Interpretability over black-box accuracy** — SHAP ensures every prediction can be explained to a business stakeholder
- **Findings over charts** — every visualization is followed by a business-language summary

---

## 👤 Author

**Prakhar**
B.Tech Computer Science | Data Analytics Portfolio Project

---

*This project is part of an ongoing effort to build data skills with a focus on business thinking, not just technical execution.*
