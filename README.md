<div align="center">

# Customer Churn Prediction & Retention Analytics

**An end-to-end customer churn analysis using Python, PostgreSQL, and Power BI**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

</div>

---

## Table of Contents

- [Project Overview](#-project-overview)
- [Project Objectives](#-project-objectives)
- [Tools & Technologies](#%EF%B8%8F-tools--technologies)
- [Project Structure](#-project-structure)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Key Performance Indicators](#-key-performance-indicators)
- [Key Business Findings](#-key-business-findings)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Business Recommendations](#-business-recommendations)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 📌 Project Overview

Customer churn is a major challenge for subscription-based businesses. Understanding why customers leave helps businesses improve customer satisfaction, strengthen retention strategies, and make better business decisions.

This project analyzes the **IBM Telco Customer Churn** dataset to identify important churn patterns across contract types, customer tenure, internet services, payment methods, monthly charges, and additional customer services.

## 🎯 Project Objectives

- Analyze customer churn and retention rates.
- Identify customer groups with high churn rates.
- Examine the relationship between contract types and churn.
- Understand churn patterns across tenure and monthly charges.
- Analyze churn by internet service and payment method.
- Build an interactive Power BI dashboard.
- Generate actionable recommendations for customer retention.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data cleaning and exploratory data analysis |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib & Seaborn | Data visualization |
| PostgreSQL | SQL-based analysis and analytical views |
| Power BI | Interactive dashboard and business reporting |
| Jupyter Notebook | Analysis workflow and documentation |
| GitHub | Version control and project portfolio |

## 📂 Project Structure

```text
Customer-Churn-Prediction/
│
├── data/
│   ├── raw/
│   │   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   │
│   └── processed/
│       └── customer_churn_cleaned.csv
│
├── notebooks/
│   └── 01_customer_churn_eda.ipynb
│
├── powerbi/
│   ├── Customer Churn Prediction & Retention Analytics.pbix
│   └── Screenshot powerbi.png
│
├── sql/
│   └── churn_analysis.txt
│
└── README.md
```

## 📊 Dataset

**Source:** IBM Telco Customer Churn

The dataset contains customer information, account details, subscribed services, billing information, tenure, and churn status.

| Metric | Value |
|---|---:|
| Total customers | 7,043 |
| Churned customers | 1,869 |
| Retained customers | 5,174 |
| Overall churn rate | 26.54% |

## 🔄 Project Workflow

1. **Data Collection:** Loaded the original Telco Customer Churn dataset.
2. **Data Cleaning:** Handled blank `TotalCharges` values and converted the column to numeric format.
3. **Exploratory Data Analysis:** Examined churn distribution, customer characteristics, services, and billing patterns using Python.
4. **SQL Analysis:** Used PostgreSQL to calculate churn metrics and analyze customer segments.
5. **Data Visualization:** Created an interactive Power BI dashboard.
6. **Business Insights:** Identified high-risk customer groups and potential retention opportunities.

## 📈 Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| Retained Customers | 5,174 |
| Churn Rate | 26.54% |
| Average Customer Tenure | 32.37 months |
| Average Monthly Charges | 64.76 |
| Average Total Charges | 2,279.73 |

> **Note:** Charge values are reported in the dataset's original units; no currency symbol is assumed.

## 🔍 Key Business Findings

### 1. Contract Type

| Contract | Churn Rate |
|---|---:|
| Month-to-month | 42.71% |
| One year | 11.27% |
| Two year | 2.83% |

> **Insight:** Customers with shorter contractual commitments are substantially more likely to churn.

### 2. Customer Tenure

| Tenure | Churn Rate |
|---|---:|
| 0–12 months | 47.44% |
| 61–72 months | 6.61% |

> **Insight:** The early customer lifecycle is a critical period for retention efforts.

### 3. Internet Service

| Internet Service | Churn Rate |
|---|---:|
| Fiber optic | 41.89% |
| DSL | 18.96% |
| No internet service | 7.40% |

> **Insight:** Fiber optic customers represent an important segment for further investigation into pricing, service quality, and customer satisfaction.

### 4. Payment Method

| Payment Method | Churn Rate |
|---|---:|
| Electronic check | 45.29% |
| Mailed check | 19.11% |
| Bank transfer | 16.71% |
| Credit card | 15.24% |

> **Insight:** Electronic check users show the highest churn rate among the payment groups.

### 5. Monthly Charges

| Monthly Charges | Churn Rate |
|---|---:|
| Low | 10.86% |
| Medium | 23.65% |
| High | 35.48% |

> **Insight:** Higher monthly charges are associated with higher churn in this dataset.

### 6. Additional Services

Customers without Online Security or Tech Support have higher churn rates than customers who subscribe to these services.

> **Insight:** Offering relevant support and security services may help improve customer retention. The relationship should be investigated further before assuming these services directly cause lower churn.

## 📊 Power BI Dashboard

The interactive dashboard presents key churn KPIs and customer churn patterns across several dimensions.

![Customer Churn Power BI Dashboard](https://github.com/SABBIR-HOSSAIN-001/customer-churn-prediction-retention-analytics/blob/main/Customer-Churn-Prediction/powerbi/Screenshot%20powerbi.png?raw=true)

**The dashboard includes:**

- Total Customers
- Churned Customers
- Retained Customers
- Churn Rate
- Churn Rate by Contract Type
- Churn Rate by Customer Tenure
- Churn Rate by Internet Service
- Churn Rate by Payment Method
- Churn Rate by Monthly Charges
- Online Security and Tech Support analysis

The `.pbix` file is available in the [`powerbi/`](Customer-Churn-Prediction/powerbi) folder.

## 💡 Business Recommendations

1. **Improve early-stage retention:** Introduce onboarding support and proactive follow-ups during the first 12 months.
2. **Encourage longer contracts:** Test suitable renewal incentives and longer-term subscription offers.
3. **Investigate fiber optic churn:** Review service quality, pricing, and customer feedback.
4. **Review electronic check payments:** Investigate payment experience and offer convenient alternative payment methods.
5. **Improve value perception:** Review pricing and communicate the benefits customers receive from higher-priced plans.
6. **Promote relevant services:** Evaluate whether Online Security and Tech Support bundles improve retention.

## 🚀 Future Improvements

- Develop a machine learning model to predict customer churn.
- Evaluate model performance using precision, recall, F1-score, and ROC-AUC.
- Identify customers with the highest predicted churn risk.
- Build a customer retention prioritization framework.
- Automate reporting and data refresh workflows.

> **Note:** Machine learning prediction is a planned future improvement, not a completed component of the current project.

## 👤 Author

**Sabbir Hossain**
Aspiring Data Analyst | Business Intelligence

[![GitHub](https://img.shields.io/badge/GitHub-SABBIR--HOSSAIN--001-181717?style=flat&logo=github&logoColor=white)](https://github.com/SABBIR-HOSSAIN-001)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sabbir%20Hossain-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sabbir-hossain-6a7149435/)

---

<div align="center">

If you find this project useful, feel free to explore the repository and share your feedback.

**Technologies:** Python · PostgreSQL · Power BI · Pandas · NumPy · Data Analytics

</div>
