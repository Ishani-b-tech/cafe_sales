# Cafe Sales Data Cleaning Project
# Project Overview
This project focuses on cleaning a messy cafe sales dataset using Microsoft Excel.
The dataset contained missing values, invalid entries, inconsistent formats, and incorrect data types. After applying structured data cleaning techniques, the dataset became suitable for reliable data analysis and visualization.

# Dataset Information
- Dataset Name: Cafe Sales Data
- Original Rows: 10,000  
- Final Rows After Cleaning: 9,943  
- Rows Removed: 57
- Columns: 8
- Tool Used: Microsoft Excel
- File Format: Excel (.xlsx)

# Columns in Dataset:
-Transaction ID
-Item
-Quantity
-Price Per Unit
-Total Spent
-Payment Method
-Location
-Transaction Date

# Data Cleaning Tasks Performed
The following data cleaning steps were applied:

# 01. Initial Data Inspection
The dataset was reviewed to understand its structure and identify potential data quality issues.

Actions Performed:

-Reviewed column names and dataset structure.
-Checked the number of rows and columns.
-Scanned for missing values and invalid entries.
-Identified columns requiring cleaning.

Key data quality issues such as missing values, invalid entries, and incomplete records were identified before applying cleaning techniques.

# 02. Fixing Data Types
Corrected column formats to ensure accurate calculations and analysis.

-Quantity - Number
-Price Per Unit - Decimal
-Total Spent - Decimal

# 03. Checking for Duplicate Records
Used Excel Remove Duplicates feature to scan all columns.
Verified that no duplicate records existed. All records were confirmed to be unique.

# 04. Handling Missing Values
Missing values were identified and handled using logical replacement methods.

Replaced missing text values with: "Not Specified"
Recalculated missing numerical values using:
  Total Spent = Quantity × Price Per Unit

This ensured numerical accuracy and data completeness.

Some records had missing values in the Item column. Instead of marking them as "Not Specified/ERROR/empty cell", logical recovery was performed using Price Per Unit.

Problem Identified:
-Some rows had missing Item names. However, Price Per Unit values were available
-Some items have a consistent unit price, allowing identification.

Action Taken:
-Analyzed known item prices.
-Matched Price Per Unit values with known item prices.
-Filled in missing Item names based on matching unit prices.

Missing Item values were logically recovered instead of being replaced with generic labels, improving dataset accuracy and usability.

# 05. Handling Invalid Values

Invalid and inconsistent values were standardized.

Replacements Applied:
  UNKNOWN → Not Specified
  Blank Cells → Not Specified
  Error → Invalid Data

This improved consistency across categorical fields

# 06. Removing Unrecoverable Rows
Removed 57 rows that contained incomplete data which could not be recovered using available methods.
Some rows contained incomplete data that could not be corrected using available cleaning methods.

Problem Identified:

-Certain rows had multiple missing critical values
-These values could not be recovered or logically replaced
-Keeping them would reduce data accuracy

Action Taken:

-Identified rows with incomplete essential fields
-Removed 57 rows that contained unusable data
-Verified that the remaining data was complete and reliable

The dataset became more reliable and suitable for analysis by removing low-quality records.

# Data Quality Improvements Summary
|  Issue | Action Taken |
|--------|--------------|
|Check duplicates|Not found|
|Missing Values|Replaced with "Not Specified"|
|Invalid Values|Standardized text values|
|Incorrect Data Types|Corrected formats|
|Incomplete Rows|Removed 57 rows|
|Data Accuracy|Recalculated missing totals|

# Files Included
-Raw Dataset :Original messy dataset
-Cleaned Dataset : Final cleaned dataset
-Documentation : Detailed cleaning steps

# Tools Used
-Microsoft Excel
-Excel Functions
-Data Validation
-Sorting & Filtering
-Pivot tables

# Project Outcome
After applying data cleaning techniques, the dataset became:

-Clean and structured
-Free from incomplete records
-Consistent across all text fields
-Accurate for calculations
-Ready for data analysis and visualization

The cleaned dataset can now be reliably used for dashboards, reporting, and business insights.

# Future Improvements
-Perform advanced data cleaning using SQL
-Build an interactive dashboard using Power BI
-Automate cleaning steps using Power Query





