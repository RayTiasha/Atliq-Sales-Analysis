# Strategic Sales & Growth Analysis for AtliQ Hardware (2020-2021)

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
1. The exponential growth of the products like Mx NB and Smash series suggests that AtliQ should reallocate marketing budget from the bottom-performing 'Home Allin1' series toward these high-momentum categories for the 2022 fiscal year. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%2010%20products.pdf)
2. While the PC division showed the highest agility with 413% growth, the P&A (Peripherals & Accessories) division remains the core of the business, contributing 56% of total 2021 revenue. This suggests that customers are buying AtliQ PCs and then filling their ecosystem with AtliQ accessories. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Division.pdf)
3. The Master series drives supply chain velocity with over 11M units sold. For 2022, I recommend maintaining high stock levels for the Master series to ensure market share. AQ HOME Allin1 (Gen 1 & 2) have the lowest demand in the entire catalog, so the remaining stock can be cleared with a bundle deal. [Link] (https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%26Bottom%205%20products.pdf)
4. Bringing in $176.2M from new products alone in a single year is a major achievement. This represents nearly 30% of the total 2021 Net Sales ($598.9M). [Link] (https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/New%20Products.pdf)
5. India is a supermarket as it generates nearly as much revenue as the USA, South Korea, and Canada combined. The North American region (USA & Canada) as a whole is a critical secondary pillar for the company. There is significant room for growth in the European market compared to the Asian and American segments. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%205%20Net%20Sales.pdf)

## Note
The original dataset is not included due to data privacy restrictions.
However, the analysis methodology and insights are fully documented.

## View the full case study here
https://raytiasha.notion.site/AtliQ-Hardware-Sales-Analytics-Case-Study-bc6377974d8183a8be4f818f1e31afa9?pvs=143

---
## 🔗 Connect with Me

**[LinkedIn](https://www.linkedin.com/in/raytiasha/) | [Email](mailto:inboxtiasha@gmail.com)**
