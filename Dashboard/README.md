 # Cafe Sales Dashboard | Power BI Portfolio Project
# Project Overview
This project presents an interactive Cafe Sales Dashboard built using Microsoft Power BI.
The goal of this project is to analyze sales performance, identify profitable products, and understand customer purchasing trends using business intelligence techniques.

The dashboard transforms raw sales data into meaningful insights through data cleaning, modeling, and DAX calculations, enabling better decision-making.
# Business Objectives
This dashboard was designed to answer key business questions:

- What is the total income and profit generated?
- Which products are the most profitable?
- Which items sell the most?
- How do sales perform across months?
- What payment methods are most used?
- What are the cost and profitability differences between products?
# Tools & Technologies Used
- Microsoft Power BI
- Power Query – Data Cleaning & Transformation
- DAX (Data Analysis Expressions) – KPI Calculations
- Data Modeling – Relationship building
- Interactive Dashboard Design
# Dataset Information
Table Name: Cafe Sales
Time Period: 2023
Data Includes:

- Transaction ID
- Item ID
- Item
- Quantity
- Price Per Unit
- Total Income
- Location
- Payment Method
- Transaction Date

Table Name: Cost
Time Period: 2023
Data Includes:

- Item ID
- Item Name
- Cost per Item
- Price Per Unit

# Data Cleaning Process
The dataset was cleaned using Power Query Editor.

Cleaning steps included:

Removing invalid and missing values
Fixing incorrect date formats
Standardizing item names
Handling null values
Creating calculated columns
Ensuring consistent data types
Removing duplicate records

These steps ensured accurate and reliable analysis.

# Data Modeling
Two tables were used:
- Cafe Sales Table
Contains transactional sales data.
- Cost Table
Contains cost per item information.

Relationships were created between:
Item ID

This enabled accurate cost and profit calculations.

# Key Performance Indicators (KPIs)
The dashboard includes several business-critical KPIs:

- Total Income
- Total Profit
- Profit Margin (%)
- Total Transactions
- Sold Quantity
- Revenue Per Item
- Highest Sold Item
- Most Profitable Item
- Total Number of Items

These KPIs provide a quick summary of overall business performance.

# Dashboard Features
The dashboard is divided into two pages:

# Page 1 — Sales Overview
This page provides a high-level summary of overall performance.

Visuals Included:
- KPI Cards (Income, Profit, Margin, Quantity)
- Profit Trend by Month
- Quantity Trend by Month
- Profit vs Cost Scatter Chart
- Payment Method Distribution
- Date Slicer
- Item Slicer
Key Insights:
- Monthly profit trends identified
- Payment method distribution analyzed
- Relationship between profit and cost visualized

# Page 2 — Product Analysis
This page focuses on product-level performance.

Visuals Included:
- Top 5 Items by Profit
- Quantity by Item
- Cost Per Item by Item
- Item Performance Table
- Highest Sold Item KPI
- Most Profitable Item KPI
Key Insights:
- Identified top-performing products
- Compared cost vs profitability
- Analyzed product sales volume

# Sample DAX Measures Used
- Profit Margin %
Profit Margin % =
DIVIDE(
    SUM('Cafe Sales'[Profit]),
    SUM('Cafe Sales'[Total Income]),
    0
)
- Most Profitable Item
Most Profitable Item =
VAR TopItem =
    TOPN(
        1,
        SUMMARIZE(
            'Cafe Sales',
            'Cafe Sales'[Item],
            "TotalProfit", SUM('Cafe Sales'[Profit])
        ),
        [TotalProfit],
        DESC
    )

RETURN
    MAXX(TopItem, 'Cafe Sales'[Item])
- Revenue Per Item
Revenue Per Item =
DIVIDE(
    SUM('Cafe Sales'[Total Income]),
    SUM('Cafe Sales'[Quantity]),
    0
)
