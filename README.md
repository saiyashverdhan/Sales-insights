# Sales Dashboard | AtliQ Hardware | Power BI,SQL

## Problem Statement

AtliQ Hardware, a leading computer hardware and peripherals manufacturer headquartered in Delhi, India, has been facing challenges in monitoring sales performance across its regional offices. The Sales Director at the headquarters currently relies on fragmented reports from regional sales managers, who often provide incomplete or overly optimistic insights through multiple Excel files. Despite these reports, overall sales have been on a decline, and the Sales Director struggles to track detailed performance metrics across different markets.

This project aims to address these challenges by developing an interactive and dynamic Power BI dashboard. The dashboard consolidates four years of sales data (2017-2020), providing the Sales Head with real-time, actionable insights into revenue, sales quantity, and profit margins across regions. With this tool, the Sales Director can make data-driven decisions, ensuring a clear and accurate view of company performance across all regions, without relying solely on manual reports from the regional managers.

## Dashboards Included
### Revenue and Sales Analysis Dashboard

- Key Metrics : ₹985M Total Revenue, 2.43M Total Sales Quantity
- Revenue by Market: Breakdown of total revenue generated across different cities, with Delhi NCR leading at ₹520M.
- Sales Quantity by Market: Comparative analysis of sales quantity per market, highlighting top-performing cities.
- Revenue Trend: A line graph showing the revenue trend over time from 2017 to early 2020, with noticeable fluctuations and an overall decline.
- Top 5 Customers: Identifies the top customers driving the highest revenue.
- Top 5 Products: Shows the most revenue-generating products, with one product far ahead of others.

### Revenue and Profit Margin Dashboard

- Revenue Contribution by Market: Region-wise revenue contribution as a percentage of the total, with Delhi NCR contributing over 50%.
- Profit Contribution % by Market: Contribution of individual market to the profit margin as ratio of specific market's margin to total margin.

- Profit % by Market: This is pure profit of each market, i.e., profit margin (selling price - cost price) divided by revenue of the market.  

        Profit contribution % is also driven by sales qty, so Delhi contributes to half the total profit margin
        but falls behind in profit made per unit level.
- Profit Margin Table: A detailed table showing customer-level revenue, profit margin contribution, and profit margin percentages.

## Lighting up the dashboard | Power BI
- Tables: Transactions, Date, Customers, Products, Markets
- Schema: Star schema with transactions table in middle and its attributes connecting to all other default tables to make sense out of the whole database. For example, market code in transactions table maps to market code and market name in Markets table.

## ETL | Power BI
- Using Power Query Editor, cleaned up data with steps like: 

    (a) Normalizing currency to INR by adding conditional column to convert USD to INR

    (b) Deleting US markets having zero sales

    (c) Changing date format in dates table to make slicer in first dashboard

    (d) Detect data types

## Data Wrangling | SQL
- Initial approach to the project was using SQL in understanding the database.
- To verify key figures visible on the dashboard, used SQL (mySQL) on the source excel files
