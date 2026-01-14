Credit Card Delinquency Risk Analysis (Power BI) 

This project analyzes credit card customers to understand delinquency risk – which customers are more likely to miss payments.

The main output is an interactive Power BI dashboard that helps risk and collections teams:
- See overall delinquency rate
- Compare risk by employment status and card type
- Analyze patterns by credit score, income, loan balance, and credit utilization

Dataset
Source: data/Delinquency_prediction_dataset.xlsx

Key columns:
- Income – customer’s monthly or annual income
- Credit_Score – numeric credit score showing creditworthiness
- Loan_Balance – current outstanding balance
- Credit_Utilization – share of available limit being used
- Debt_to_Income_Ratio – total debt divided by income
- Employees_Status – employment type (salaried, self-employed, etc.)
- Credit_Card_Type – type of card (Silver, Gold, Platinum, etc.)
- Missed_Payments – count of missed payments
- Delinquent_Account – 1 if the account is delinquent, 0 otherwise

KPIs:
- Delinquency Rate: Out of all customers, what percentage are currently delinquent (have a delinquent account)?
- Average Missed Payments: On average, how many payments each customer has missed. Higher average means customers are struggling more with their payments.
- Debt-to-Income Ratio: How big their debt is compared to their income. If it’s high, it means the customer is heavily loaded with debt and might be more likely to miss payments.
- Credit Utilization: How much of their available credit they are using. For example, if someone has a limit of 1,00,000 and is using 80,000, utilization is 80%. High utilization can be a warning sign.

What I did
- Cleaned and explored the data (handled missing income, credit score, and loan balance).
- Created calculated columns for credit score bands, utilization bands, and risk buckets (Low / Medium / High).
- Built DAX measures for delinquency rate, total customers, delinquent customers, and average missed payments.
- Designed a Power BI dashboard with pages for:
  - Overall KPIs
  - Risk by employment status
  - Risk by card type

Why Power BI?
- I used Power BI because the main goal was to give business users (risk and collections teams) an interactive view of delinquency risk. Power BI makes it easy for them to slice by employment status or card type without needing SQL or Python.

  -	I used a bar chart for delinquency rate by employment status because it’s simple to compare categories side-by-side and rank which group is riskier.
  -	I used a stacked column or 100% stacked bar for risk buckets because it clearly shows the distribution (low/medium/high risk) within each group, like each card type.
  -	I used cards for KPIs (total customers, delinquency rate) so that decision-makers can see the key numbers instantly at the top without reading tables.

who will use this?
-	This dashboard is mainly for the credit risk team and collections managers. They need to know which customer segments are most likely to default.
-	It could also be used by product managers for credit cards to understand which card types attract riskier customers and whether to adjust features or limits.
-	Senior management can use the high-level KPIs and risk bucket view to monitor portfolio health.

Files
- data/Delinquency_prediction_dataset.xlsx – source dataset
- powerbi/Credit_Delinquency_Dashboard.pbix – Power BI report
- docs/dashboard_screenshot.png – sample dashboard view

How to open
1. Download or clone this repository.
2. Open powerbi/Credit_Delinquency_Dashboard.pbix in Power BI Desktop.
3. Explore the different pages and slicers to see risk patterns. 