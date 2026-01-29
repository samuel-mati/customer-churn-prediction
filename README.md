# 📉 Telco Customer Churn Analysis & Prediction

## Executive Summary
Customer churn is a major revenue risk for subscription-based telecom companies.  
This project analyzes customer behavior, builds a machine learning churn prediction model, and presents actionable insights through an interactive Power BI dashboard.

🔗 **Dashboard Overview (Power BI):**  
👉 https://app.powerbi.com/view?r=XXXXXXXX  
*(Replace with your published dashboard link)*

---

## Business Problem
Telecom customers often churn early due to contract flexibility, pricing, or service dissatisfaction.  
The business needs to:
- Identify customers at high risk of churn
- Understand key churn drivers
- Focus retention efforts where they matter most

---

## Dataset Overview
- **Records:** 7,043 customers  
- **Target Variable:** `Churn` (Yes / No)

### Feature Categories
- Customer demographics
- Contract & billing details
- Internet and service subscriptions
- Tenure and billing charges

---

## Tools & Technologies
**Data & Modeling**
- Python
- Pandas, NumPy
- Scikit-learn

**Visualization**
- Power BI
- Matplotlib / Seaborn

---

## Exploratory Data Analysis (EDA)
Key insights:
- Churn peaks at **low tenure**
- Customers with **higher monthly charges (≈75–100)** churn more
- **Low total charges** correspond to early churn
- Month-to-month contracts and electronic check payments show higher churn rates

---

## Data Preprocessing
- Binary categorical variables encoded as `0 / 1`
- Multi-category features one-hot encoded
- Reference categories dropped to avoid redundancy

**Final dataset shape:**  
`7,043 rows × 32 features`

---

## Machine Learning Model
- **Model:** Gradient Boosting Classifier
- **Train/Test Split:** 80% / 20%

### Model Performance (Test Set)

| Metric | Value |
|------|------|
| Accuracy | **0.80** |
| Precision (Churn) | **0.66** |
| Recall (Churn) | **0.51** |
| F1-Score (Churn) | **0.57** |

---

## Confusion Matrix Summary

| Outcome | Count |
|------|------|
| True Negatives | 935 |
| False Positives | 100 |
| False Negatives | 183 |
| True Positives | 191 |

**Key Insight:**  
The model predicts non-churners reliably, but some churned customers are missed — highlighting opportunities for recall improvement.

---

## Feature Importance (Top Drivers)
1. Tenure
2. Internet Service – Fiber Optic
3. Payment Method – Electronic Check
4. Contract Type – Two Year
5. Total Charges
6. Monthly Charges

These drivers align with both EDA findings and business intuition.

---

## Power BI Dashboard
The dashboard translates analytical findings into business-ready visuals.

### Page 1 – Churn Overview
- Overall churn rate
- Churn by contract type
- Churn by payment method
- Service-level churn patterns

### Page 2 – High-Risk Segments
- Churn rate (Month-to-Month customers)
- Churn rate (Electronic Check users)
- Average tenure of churned customers
- Churn by contract type & tenure buckets

**Design Theme**
- Page background: `#ECF9F1`
- Green = positive / retained
- Red = churn risk
- Consistent KPI and chart styling

---

## Limitations & Future Work
**Limitations**
- Moderate recall for churn prediction
- No cost-sensitive optimization
- Class imbalance not explicitly handled

**Future Improvements**
- Recall-focused tuning
- Cost-based evaluation
- Threshold optimization
- Deployment as a retention decision-support tool

---



## How to Run
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
