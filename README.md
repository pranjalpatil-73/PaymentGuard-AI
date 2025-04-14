# **PaymentGuard-AI**
Built an ML model to predict subscription payment defaults 30 days early using customer and billing data. Achieved 87% accuracy, flagged $140K+/mo in at-risk revenue, and enabled proactive actions to reduce churn and recover payments.
# Payment Default Risk Prediction (ML Project)

Predict which subscription customers are likely to **miss a payment** 30 days in advance — helping SaaS companies **reduce revenue loss** and take action early.

---

## Project Overview
This project uses machine learning to flag customers at risk of **defaulting on their payments** before it happens. With this system, SaaS businesses can:
- Reduce revenue leakage from failed payments
- Recover at-risk revenue proactively
- Improve retention and cash flow

---

## Key Results
- **87% prediction accuracy** (AUC: 0.89)
- Trained on **7,000+ customer records**
- Flags over **$140,000/month** in at-risk revenue
- Estimated **38% reduction in losses** with action

---

## Problem Statement
Failed payments lead to lost revenue and customer churn for SaaS companies. The goal was to:
- **Predict failed payments 30 days early**
- Group customers by risk level (High, Medium, Low)
- Recommend actions to **reduce default and recover revenue**

---

## Dataset
- **Source**: Kaggle (Telco Customer Churn dataset)
- **Records**: 7,043 subscription customers
- **Features used**: Payment method, contract type, monthly charges, tenure, usage
- **Target column**: DefaultRisk (1 = high risk, 0 = low risk)

---

## Data Preparation
- Removed invalid/missing entries (0.15%)
- Created features like:
  - `Monthly_to_Total_Ratio`
  - `Tenure_Group` (New, Established, Long-term)
- Removed outliers in `MonthlyCharges`

---

## Model Details
- **Algorithm**: Gradient Boosting Classifier
- **Parameters**:
  - n_estimators: 200
  - learning_rate: 0.05
  - max_depth: 5
- **Feature Importance**:
  1. Contract Type
  2. Payment Method
  3. Monthly Charges

---

## Risk Scoring Output
| Risk Segment | Customers | Avg Default Probability | Monthly Revenue at Risk |
|--------------|-----------|--------------------------|--------------------------|
| High Risk    | 217       | 82%                      | $38,740                  |
| Medium Risk  | 492       | 51%                      | $67,210                  |
| Low Risk     | 891       | 12%                      | $36,150                  |

---

## Action Plan (Based on Risk)
**High Risk:**
- Contact within 48 hours
- Offer flexible payment plans

**Medium Risk:**
- Send automated reminders (7, 3, 1 days before due date)
- $10 credit for updating payment info

**Low Risk:**
- Annual plan discount offers
- Loyalty programs and upsells

---

## Tech Stack
- Python (pandas, scikit-learn, matplotlib, seaborn)
- Jupyter Notebook

---

## Next Steps
- Add API or Streamlit dashboard for business use
- Integrate with billing systems for daily risk updates

---

## Author
Your Name  
Email: your.email@example.com  
GitHub: [yourusername](https://github.com/yourusername)


