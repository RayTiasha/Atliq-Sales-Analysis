# AtliQ Hardware's Sales Performance Analysis

## Project Objective
The Sales Director at Atliq Hardware requires immediate visibility into key business metrics to support strategic decision-making and drive business growth. Currently, leadership team lacks centralized tracking for revenue, making it difficult to identify underperforming markets and pinpoint growth opportunities.

## Tool used
Microsoft Excel

## KPIs
- Net Sales (Gross Sales minus returns, allowances, and discounts).
- Analysis Dimensions at Geographic Region and Product Category.
- Year-over-Year (YoY) Growth Percentage to isolate underperforming markets and target 2022 opportunities.
  
## Data Methodology
1. Data Cleaning & ETL - Utilized Power Query to handle missing values, resolve nulls, and standardize inconsistent customer naming conventions.
2. Data Modeling - Implemented a robust Star Schema by separating transactional data into Fact tables and used dedicated Dimension tables.
3. Time Intelligence - Established a dedicated Date dimension table to enable seamless, standardized time-comparison logic.
4. Analytical Calculations - Programmed custom DAX Measures (Power Pivot) to standardize business logic and automate the calculation of Net Sales and YoY Growth.

## Dataset Structure

![AtliQ Hardware Star Schema](reports/Schema%20Diagram.png)

## Technical Implementation
The following calculations were implemented in Power Pivot to standardize business logic:

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
## Business Insights
The model revealed five critical pillars for AtliQ’s 2022 strategy:

1. The exponential growth of the products like Mx NB and Smash 2 suggests that AtliQ should allocate good marketing budget toward these high-momentum categories for the 2022 fiscal year. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%2010%20products.pdf)
2. While the PC division showed the highest agility with 413% growth, the P&A (Peripherals & Accessories) division remains the core of the business, contributing 56% of total 2021 revenue. This suggests that customers are buying AtliQ PCs and then filling their ecosystem with AtliQ accessories. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Division.pdf)
3. The Master series drives supply chain velocity with over 11M units sold. For 2022, I recommend maintaining high stock levels for the Master series to ensure market share. AQ HOME Allin1 (Gen 1 & 2) have the lowest demand in the entire catalog, so the remaining stock can be cleared with a bundle deal. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%26Bottom%205%20products.pdf)
4. Bringing in $176.2M from new products alone in a single year is a major achievement. This represents nearly 30% of the total 2021 Net Sales ($598.9M). [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/New%20Products.pdf)
5. India is a super-market as it generates nearly as much revenue as the USA, South Korea, and Canada combined. The North American region (USA & Canada) as a whole is a critical secondary pillar for the company. There is significant room for growth in the European market compared to the Asian and American segments. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%205%20Net%20Sales.pdf)

## Recommendations
1. Shift capital from saturated, underperforming regions and balance the budget toward high-growth geographical territories identified in 2022.
2. Design a targeted retention and loyalty program specifically for the top 5 revenue-generating clients to maximize customer lifetime value (CLV).
3. Formulate an exit strategy or gradual phase-out plan for stagnant, unused inventory within the Electronics category to lower holding costs and free up working capital.

## Report

<img width="2000" height="1600" alt="Untitled design" src="https://github.com/user-attachments/assets/99c703ab-8baf-4b35-b611-ff3187e771d8" />

## Note
The original dataset is not included due to data privacy restrictions.
However, the analysis methodology and insights are fully documented.
