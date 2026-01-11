Credit Card Delinquency Risk Analysis (Power BI)

This project analyzes credit card customers to understand delinquency risk – which customers are more likely to miss payments.

The main output is an interactive Power BI dashboard that helps risk and collections teams:
- See overall delinquency rate
- Compare risk by employment status and card type
- Analyze patterns by credit score, income, loan balance, and credit utilization

Dataset
Source: `data/Delinquency_prediction_dataset.xlsx`

Key columns:
- `Income` – customer’s monthly or annual income
- `Credit_Score` – numeric credit score showing creditworthiness
- `Loan_Balance` – current outstanding balance
- `Credit_Utilization` – share of available limit being used
- `Debt_to_Income_Ratio` – total debt divided by income
- `Employees_Status` – employment type (salaried, self-employed, etc.)
- `Credit_Card_Type` – type of card (Silver, Gold, Platinum, etc.)
- `Missed_Payments` – count of missed payments
- `Delinquent_Account` – 1 if the account is delinquent, 0 otherwise

What I did
- Cleaned and explored the data (handled missing income, credit score, and loan balance).
- Created calculated columns for credit score bands, utilization bands, and risk buckets (Low / Medium / High).
- Built DAX measures for delinquency rate, total customers, delinquent customers, and average missed payments.
- Designed a Power BI dashboard with pages for:
  - Overall KPIs
  - Risk by employment status
  - Risk by card type

Files
- `data/Delinquency_prediction_dataset.xlsx` – source dataset
- `powerbi/Credit_Delinquency_Dashboard.pbix` – Power BI report
- `docs/dashboard_screenshot.png` – sample dashboard view

How to open
1. Download or clone this repository.
2. Open `powerbi/Credit_Delinquency_Dashboard.pbix` in Power BI Desktop.
3. Explore the different pages and slicers to see risk patterns.