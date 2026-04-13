# Atliq-Sales-Analysis
Sales analysis identifying growth drivers using Excel
Atliq Hardware Sales Analysis
Project Overview

AtliQ Hardware faced the challenge of extracting actionable insights from a massive dataset of ~800,000 sales records. This project leverages Excel’s Power Pivot and Power Query to bypass traditional spreadsheet limitations, transforming raw data into a high-performance analytical tool. By modeling complex data relationships, I identified key growth drivers and regional profitability leaks, providing the Sales Director with a scalable solution for 2022 strategy planning.

## Business Questions Answered
1. What are the top 10 products by growth?
2. Which divisions performed best?
3. Which products ranked Top 5 and Bottom 5 by demand?
4. What new products were introduced in 2021?
5. What are the Top 5 countries by net sales?

## Tool Used
Microsoft Excel
## Features
Power Query, Power Pivot (Data Modeling), DAX, Pivot Tables, Advanced Conditional Formatting.

## Data Modeling
Created a Star Schema with Fact_Sales connected to Dim tables (Products, Customers, Markets).
Established a Date Table using Power Pivot to enable Time Intelligence analysis.

<img width="1777" height="797" alt="image" src="https://github.com/user-attachments/assets/d041b446-b4be-42c4-b8d6-a9a406503265" />

## Key Calculated Measures
To drive the analysis, I developed several DAX measures within the Excel Data Model. Here are a few examples of the core business logic:
1. Net Sales = SUM(fact_sales_monthly[net_sales_amount])
2. Net Sales 2020 = CALCULATE([Net Sales],dim_date[FY]="2020")
3. Net Sales 2021 = CALCULATE([Net Sales],dim_date[FY]="2021")
4. Variance = DIVIDE([NetSales 21],[NetSales 20],0)

## Approach
Utilized Power Query to perform advanced ETL processes, including data pivoting, type transformation, and handling inconsistent data formats from multiple CSV sources.
Aggregated net sales using DAX measures.
Applied Top & Bottom value filters to identify demand trends, analyze product growth, and compare sales performance.

## Key Insights & Findings
Top 10 products drove majority of growth
Select divisions contributed most to revenue increase
Demand concentrated among few high-performing products
New products showed promising adoption
Top 5 countries generated highest revenue

## Note
The original dataset is not included due to data privacy restrictions.
However, the analysis methodology and insights are fully documented.

## View the full case study here
https://raytiasha.notion.site/AtliQ-Hardware-Sales-Analytics-Case-Study-bc6377974d8183a8be4f818f1e31afa9?pvs=143

---
## 🔗 Connect with Me

**[Portfolio](https://raytiasha.notion.site/Tiasha-Ray-f26377974d8183abb9b7016970a13367) | [LinkedIn](https://www.linkedin.com/in/raytiasha/) | [Email](mailto:inboxtiasha@gmail.com)**
