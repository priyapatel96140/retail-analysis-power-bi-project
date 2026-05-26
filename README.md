# Retail Sales & Profitability Analysis

This is a personal data project where I analyzed retail transaction data across multiple store chains, categories, and geographic regions. I built a dynamic dashboard to track how different product categories perform and where the business is making (or losing) money.

## Brief Summary
An end-to-end analytics project tracking unit sales, profit margins, and regional performance across multiple retail chains to find which store models and item categories are the most profitable.

## Overview
I took raw transactional retail data, mapped it to separate dimension tables (like geography and dates), and created a relational data model. From there, I calculated core retail metrics—like total revenue, cost, and profit margins—and built an interactive executive dashboard to visualize sales trends across different states, store managers, and shopping categories.

## Problem Statement
Multi-chain retail companies generate massive amounts of daily sales data, but raw revenue numbers don't show the full picture. A category might have high sales volume but terrible profit margins due to high costs. This project solves a few specific problems:
1. Identifying which product lines (e.g., Clothing, Home, Shoes) actually drive the highest net profit rather than just high revenue.
2. Spotting operational underperformance by tracking sales and profit margins across different store managers and states.
3. Consolidating monthly transactional updates (like adding new August data) cleanly into an existing data model without breaking metrics.

## Dataset
The project utilizes a relational structure consisting of both transactional and lookup data:
* **Fact Table / Aug Data:** Transactional records containing `Date`, `Chain` (e.g., Ready Wear, Bellings), `Postcode`, `Category`, `Total Units`, `Sale Price`, and `Cost Price`.
* **Dim Tables (Lookups):** Geographic data linking `Postcode` to `Suburb`, `State`, and `Store Manager`, alongside product categories and financial calendars.

## Tools & Technologies
* **Data Modeling & Calculations:** Power BI Desktop / Excel (Power Pivot)
* **DAX / Formulas:** Used for calculating custom retail metrics (Revenue, Profit, Margins)
* **Data Transformation:** Power Query (for merging tables and appending monthly data updates)
* **Version Control:** Git & GitHub

## Method (How I Built This)
1. **Data Modeling:** Instead of working with one giant, messy sheet, I split the data into a clean Star Schema. I connected the main transaction table (`Fact Table`) to the lookup tables (`Dim Tables`) using common fields like `Postcode` and `Date`.
2. **Handling Updates:** I used Power Query to cleanly append the new monthly records (`Aug Data`) into the main sales history table, making sure the formatting matched perfectly.
3. **Writing Custom Metrics:** I wrote calculations to track business health, including:
   * **Total Revenue:** `Units Sold * Sale Price`
   * **Total Cost:** `Units Sold * Cost Price`
   * **Total Profit:** `Revenue - Cost`
   * **Profit Margin (%):** To see exactly how many cents of profit we keep for every dollar earned.
4. **Dashboard Layout:** I designed a clean, user-friendly layout. I put the high-level performance cards at the top, trend lines in the middle to show performance over time, and regional/manager breakdowns at the bottom so users can filter the data with a single click.

## Key Insights
* **Revenue vs. Margin:** Certain high-volume categories like "Groceries" or "Home" move a lot of units, but clothing categories like "Womens" and "Mens" fashion often yield significantly higher profit margins.
* **Top-Performing Chains:** The performance varies wildly between different chains (like *Ready Wear* vs. *Bellings*), showing that pricing strategies or target audiences heavily impact profitability.
* **Regional Highlights:** Mapping the postcodes revealed that certain states and specific store managers consistently hit their margin targets, while others struggle with high overhead/cost prices.

## Dashboard Output
Here is a look at the final analytics dashboard:

https://github.com/priyapatel96140/retail-analysis-power-bi-project/blob/main/retail-analysis-webinar-dashboard.png

*Quick stats from the view:*
* Clean breakdown of performance metrics by **State**, **Category**, and **Manager**.
* Fully interactive charts allowing you to drill down into specific retail chains or time periods.

## How to Run this Project
1. Download the `.pbix` file
2. Open the file in Power BI Desktop
3. Refresh the dataset if required
4. Interact with filters and visuals
