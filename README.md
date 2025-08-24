## 📊 Credit Risk & Customer Retention Analysis

### Project Overview

This project analyzes 1,000 bank customers to identify drivers of loan default and customer churn. Using EDA, feature engineering, predictive modeling, and dashboarding in Power BI, the goal was to provide actionable insights for stakeholders to reduce financial risk and improve customer retention.

### Business Problem

- Loan Defaults: Missed repayments increase financial risk and reduce profitability.
- Customer Churn: High churn rates impact revenue and increase acquisition costs.
- Need: Early identification of high-risk customers and data-driven strategies to improve retention.

### Dataset Overview

- Customers: 1,000 (synthetic but realistic dataset)
- Key Features:
  - Demographics - Age, Gender, Income Bracket, Employment Status, City
  - Credit & Loan - Credit Score, Loan History, Loan Amount, Credit Utilization
  - Engagement - Mobile App Usage, Net Banking Usage, Complaints, Offers Response
  - Investments - FD Investment, Insurance, Credit Card ownership
- Target Variables:
  - Default_Flag - Whether customer defaulted on loans.
  - Churn_Flag - Whether customer churned from the bank.

### Exploratory Data Analysis (EDA) — Key Insights

- Majority of customers are 25–64 years old.
- Credit Scores are mostly between 600–750; <500 are high risk.
- Loan History: Customers with 3–5 loans → 28% default rate; 6+ loans → 23%.
- Credit Utilization: >60% utilization linked to higher default probability.
- Complaints: Surprisingly, customers with 3+ complaints had lower churn (likely due to effective resolution).
- Response to Offers: No strong impact on churn; customer experience matters more.

### Feature Engineering

- Expense-to-Income Ratio = Monthly Expense ÷ Monthly Income.
- High-Risk Flag = Based on Credit Score <600, Utilization >60%, Multiple Loans, Overdue Days >30.
- Created categorical bands for Credit Score, Age Groups, and Utilization.

### Predictive Modeling

- Models tested: Logistic Regression, Random Forest, XGBoost.
- Challenge: Strong class imbalance (Defaults ~14%, Churn ~16%).
- Techniques applied:
  - SMOTE (Synthetic Oversampling).
  - Threshold tuning to improve recall.
- Results:
  - Default model recall improved (up to 75%) → useful as an early-warning system.
  - Churn models underperformed due to lack of rich behavioral features.
  - Precision remained weak - models generate more “false alarms”.

### Power BI Dashboard

- Built an interactive dashboard with multiple pages:
- Executive Overview - KPIs (Default Rate, Churn Rate, High-Risk Customers).
- Credit Risk Analysis - Credit Score Distribution, Utilization vs Default Rate, Loan History vs Defaults.
- Customer Engagement - Complaints vs Churn, Response to Offers, Digital Engagement.
- High-Risk Customers - Breakdown by City, Income Bracket, Loan History; drill-down to customer level.
- Predictive Insights - Model-powered risk flagging (recall-focused).

 ### Recommendations for Stakeholders

- Credit Risk Monitoring
  - Closely monitor customers with low scores, high utilization, or multiple loans.
  - Strengthen collection strategies for delinquent customers.
- Customer Retention
  - Improve complaint resolution speed → directly linked to lower churn.
  - Tailor offers to income/city segments rather than blanket campaigns.
- Data Strategy
  - Collect richer behavioral and temporal data (repayment history, service resolution times, surveys).

### Business Impact

- Reduce loan losses by identifying risky customers earlier.
- Improve retention through better experience management.
- Lower costs via targeted campaigns instead of broad acquisition.
- Enable proactive decision-making with real-time dashboard monitoring.

### Tech Stack

- Languages & Libraries: Python (pandas, numpy, scikit-learn, imbalanced-learn, xgboost, matplotlib, seaborn)
- Database: Snowflake SQL (for data aggregation & joins)
- Visualization: Power BI (KPIs, DAX measures, interactive dashboards)
- Tools: Jupyter Notebook, GitHub

### Contact

Shijin Ramesh
Email: kshijin92@mail.com  
[LinkedIn](https://www.linkedin.com/in/shijinramesh/) | [Portfolio](https://www.shijinramesh.co.in/)
