# 📊 Customer Retention Analysis — Telco Churn Study

> End-to-end Data Analyst project: **EDA → SQL Analysis → ML Churn Prediction** on 7,000+ telecom customers to identify churn drivers and build a risk-scoring system.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

---

## 🔍 Problem Statement

A telecom company is losing ~26.5% of its customers every year. This project answers:
- **Why** are customers churning?
- **Who** is most at risk of churning next?
- **What** can the business do about it?

---

## 🗂️ Project Structure

```
Customer-Retention-Analysis/
├── data/
│   └── telco_churn.csv          # IBM Telco Customer Churn dataset
├── notebooks/
│   ├── 01_EDA.ipynb             # Exploratory Data Analysis
│   ├── 02_SQL_Analysis.ipynb    # SQL-based business questions
│   └── 03_ML_Model.ipynb        # Churn prediction + risk scoring
├── dashboard/
│   └── churn_dashboard.twbx     # Tableau dashboard
├── requirements.txt
└── README.md
```

---

## 🚀 Key Results

| Metric | Value |
|---|---|
| Dataset size | 7,043 customers |
| Overall churn rate | 26.5% |
| Best model accuracy | ~80% (Gradient Boosting) |
| Best ROC-AUC | ~0.84 |
| Monthly revenue at risk | ~$139,000 |
| Estimated annual revenue at risk | ~$1.67 million |

---

## 📓 Notebook Breakdown

### 01 — Exploratory Data Analysis
- Churn distribution (pie + bar charts)
- Contract type vs churn rate
- Tenure distribution by churn status
- Monthly charges vs churn
- Service usage (TechSupport, OnlineSecurity, StreamingTV) vs churn
- Correlation heatmap

### 02 — SQL Analysis (SQLite via Python)
- Overall churn rate query
- Churn by contract type
- Revenue lost to churn (monthly + annual)
- Churn by payment method
- High-value at-risk customers (high spend + short tenure)
- TechSupport impact on churn rate

### 03 — ML Churn Prediction
- Feature engineering + label encoding
- 3 models trained: Logistic Regression, Random Forest, Gradient Boosting
- ROC curves + confusion matrix
- Feature importance analysis
- **Churn Risk Scoring** — customers segmented into Low / Medium / High risk

---

## 🔑 Top 3 Churn Drivers

| # | Driver | Finding |
|---|---|---|
| 1 | **Contract Type** | Month-to-month customers churn at 42.7% vs 2.8% for 2-year contracts |
| 2 | **Tenure** | Median churned customer leaves at ~10 months vs ~38 months for retained |
| 3 | **Monthly Charges** | Churned customers pay avg $74/mo vs $61/mo for retained customers |

---

## 💡 Business Recommendations

- 🎯 **Target High Risk segment** (60%+ churn probability) with proactive retention offers before they leave
- 📝 **Offer long-term contract incentives** to month-to-month customers at months 3–6
- 💰 **Introduce loyalty pricing** for high monthly charge customers after 6 months
- 🛠️ **Bundle TechSupport for free** during onboarding — absence doubles churn risk
- 💳 **Investigate electronic check users** — they churn at 45%, highest of all payment methods

---

## 📊 Tableau Dashboard

The Tableau dashboard covers:
- Overall KPIs (churn rate, revenue at risk, avg tenure)
- Churn breakdown by contract, payment method, and internet service
- Tenure vs churn heatmap
- High-risk customer table

---

## 🛠️ Setup & Run

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/Customer-Retention-Analysis.git
cd Customer-Retention-Analysis
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Get the dataset from Kaggle:
👉 [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

Rename the file to `telco_churn.csv` and place it in the `data/` folder.

### 4. Run notebooks in order
```
01_EDA.ipynb → 02_SQL_Analysis.ipynb → 03_ML_Model.ipynb
```

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
sqlalchemy
jupyter
```

---

## 📁 Dataset

**Source:** [IBM Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
**Rows:** 7,043 customers  
**Features:** 21 columns including demographics, services subscribed, contract type, charges, and churn label
