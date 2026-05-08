# AtliQ Hardware Sales Analysis

## Problem Statement
Sales Director at Atliq Hardware needed immediate visibility into the following questions to drive business growth:
- Revenue by region/product
- Underperforming markets/customers  
- Growth opportunities for 2026
  
## My Approach
1. Leveraged Power Query for fixing null values and standardize customer names.
2. Implemented a Star Schema using Power Query for Data Modeling, with "Fact_Sales" at the center.
3. Established a dedicated Dim_Date table to enable seamless YoY (Year-over-Year) comparisons.
4. Developed calculated measures to standardize business logic across the organization (e.g., Net Sales, Variance %, and FY 20/21 Performance).

![AtliQ Hardware Star Schema](reports/Schema%20Diagram.png)

<img width="2000" height="1600" alt="Untitled design" src="https://github.com/user-attachments/assets/99c703ab-8baf-4b35-b611-ff3187e771d8" />

## Key Calculated Measures
To drive the analysis, I developed several DAX measures within the Excel Data Model. Here are a few examples of the core business logic:
1. Net Sales = SUM(fact_sales_monthly[net_sales_amount])
2. Net Sales 2020 = CALCULATE([Net Sales],dim_date[FY]="2020")
3. Net Sales 2021 = CALCULATE([Net Sales],dim_date[FY]="2021")
4. Variance = DIVIDE([NetSales 21],[NetSales 20],0)
```Code Snippet
Net Sales 2021 = 
CALCULATE(
    [Net Sales],
    dim_date[FY] = "2021"
)
```
## Key Findings
The model revealed five critical pillars for AtliQ’s 2022 strategy:

1. The exponential growth of the products like Mx NB and Smash 2 suggests that AtliQ should allocate good marketing budget toward these high-momentum categories for the 2022 fiscal year. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%2010%20products.pdf)
2. While the PC division showed the highest agility with 413% growth, the P&A (Peripherals & Accessories) division remains the core of the business, contributing 56% of total 2021 revenue. This suggests that customers are buying AtliQ PCs and then filling their ecosystem with AtliQ accessories. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Division.pdf)
3. The Master series drives supply chain velocity with over 11M units sold. For 2022, I recommend maintaining high stock levels for the Master series to ensure market share. AQ HOME Allin1 (Gen 1 & 2) have the lowest demand in the entire catalog, so the remaining stock can be cleared with a bundle deal. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%26Bottom%205%20products.pdf)
4. Bringing in $176.2M from new products alone in a single year is a major achievement. This represents nearly 30% of the total 2021 Net Sales ($598.9M). [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/New%20Products.pdf)
5. India is a super-market as it generates nearly as much revenue as the USA, South Korea, and Canada combined. The North American region (USA & Canada) as a whole is a critical secondary pillar for the company. There is significant room for growth in the European market compared to the Asian and American segments. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%205%20Net%20Sales.pdf)

## Business Recommendations
1. Balance marketing budget for different regions.
2. Customer tier program for top 5 customers.
3. Phase out Electronics for unused products.

## Note
The original dataset is not included due to data privacy restrictions.
However, the analysis methodology and insights are fully documented.

---
## 🔗 Find Me Online

**[LinkedIn](https://www.linkedin.com/in/raytiasha/) | [Portfolio](https://raytiasha.carrd.co/) | [Email](mailto:inboxtiasha@gmail.com)**
