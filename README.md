# AtliQ Hardware's Sales Performance Analysis

## Project Background
Atliq Hardware manufactures computers, peripherals, and storage products for markets across the APAC, EMEA, and NA regions. The Sales Director wants to understand underperforming markets based on net sales from the previous two years and identify growth opportunities so that he can make informed decisions about product allocation for the upcoming year, 2022.

Insights and recommendations are provided based on the following key areas:
- Net Sales (Gross Sales minus returns, allowances, and discounts).
- Analysis Dimensions at Geographic Region and Product Category.
- Year-over-Year (YoY) Growth Percentage to isolate underperforming markets and target 2022 opportunities.

## Data Structure Overview
This analysis used data representing customers, product categories, markets, and sales from 2020 to 2021.<br>

**1. Customer Data** - Contains customer-related information such as customer names, customer codes and market regions.<br>
**2. Product Data** - Includes product details such as product names, product categories, product codes, and divisions(computers/peripherals/storage).<br>
**3. Market Data** - Contains market(country) and regional information.<br>
**4. Sales Data** - Includes transactional sales records such as sales quantity, net sales amount, dates, customer codes, and product codes.

![AtliQ Hardware Star Schema](reports/Schema%20Diagram.png)

## Executive Summary

AtliQ’s net sales performance across customers, products, markets, and divisions for the years 2020 and 2021 highlights strong growth in key product categories such as Mx NB, Smash 2, and the Master series, indicating high customer demand and strong product-market fit. The PC division recorded significant year-over-year growth, while the Peripherals & Accessories (P&A) division remained the largest revenue contributor, accounting for over half of total sales in 2021.

At the market level, India emerged as the top-performing region, generating revenue comparable to the combined contribution of the USA, South Korea, and Canada. North America continues to be a critical secondary market, while other regions show potential for further growth.

New product launches contributed nearly 30% of total net sales in 2021, demonstrating their strong impact on overall business performance. At the same time, certain products such as AQ HOME Allin1 (Gen 1 & 2) showed weak demand and may require strategic review.

Overall, the findings suggest that AtliQ’s sales growth can be driven by focusing on high-performing products and markets, strengthening the P&A ecosystem, scaling successful new launches, and optimizing or reducing investment in low-demand products to improve overall efficiency and revenue contribution.

<img width="2000" height="1600" alt="Untitled design" src="https://github.com/user-attachments/assets/99c703ab-8baf-4b35-b611-ff3187e771d8" />

## Tool used
Microsoft Excel

## Data Methodology
1. Data Cleaning & ETL - Utilized Power Query to handle missing values, resolve nulls, and standardize inconsistent customer naming conventions.
2. Data Modeling - Implemented a robust Star Schema by separating transactional data into Fact tables and used dedicated Dimension tables.
3. Time Intelligence - Established a dedicated Date dimension table to enable seamless, standardized time-comparison logic.
4. Analytical Calculations - Programmed custom DAX Measures (Power Pivot) to standardize business logic and automate the calculation of Net Sales and YoY Growth.

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

1. Products such as Mx NB and Smash 2 recorded strong sales growth, indicating high customer demand within these categories. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%2010%20products.pdf)
2. The PC division recorded the highest year-over-year growth at 413%, while the P&A (Peripherals & Accessories) division contributed 56% of total 2021 revenue. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Division.pdf)
3. The Master series achieved over 11 million units sold, making it the highest-volume product series in the portfolio. In contrast, AQ HOME Allin1 (Gen 1 & 2) recorded the lowest sales performance. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%26Bottom%205%20products.pdf)
4. New products generated $176.2M in revenue during 2021, contributing nearly 30% of the company’s total net sales of $598.9M. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/New%20Products.pdf)
5. India emerged as the highest-performing market, generating revenue nearly equal to the combined contribution of the USA, South Korea, and Canada. Additionally, the North American market (USA & Canada) remained a significant contributor to total sales. [Link](https://github.com/RayTiasha/Atliq-Sales-Analysis/blob/main/reports/Top%205%20Net%20Sales.pdf)

## Recommendations
1. Increase focus on high-performing product categories such as Mx NB and Smash 2 by aligning marketing and sales efforts toward products with strong growth momentum.
2. Continue strengthening the P&A (Peripherals & Accessories) division, as it contributes the majority share of total revenue and remains a key business driver.
3. Maintain sufficient inventory levels for high-demand products such as the Master series to support continued sales performance and avoid stock shortages.
4. Reassess the performance of low-demand products such as AQ HOME Allin1 (Gen 1 & 2) and consider promotional strategies or inventory optimization to reduce excess stock.
5. Prioritize investment and expansion efforts in high-performing markets such as India and North America while exploring additional growth opportunities in other regions.

## Note
The original dataset is not included due to data privacy restrictions.
However, the analysis methodology and insights are fully documented.

---

For more of my projects and data journey, visit my [Portfolio](https://raytiasha.github.io/Portfolio/).
