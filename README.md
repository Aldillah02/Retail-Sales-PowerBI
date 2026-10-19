# Retail-Sales-PowerBI
Retail sales analysis using Power BI, Power Query, and DAX, covering sales trends, product categories, payment methods, and sales channels.
# Retail Sales Dashboard | Power BI

## Project Overview
This project analyzes retail sales using Power BI. It covers data cleaning with Power Query, calculations with DAX, and an interactive dashboard for exploring sales performance.

## Dataset
- Source: Kaggle — Retail Store Sales dataset
- Total transactions: 12,575
- Period: 1 January 2022–18 January 2025
- Data includes product categories, payment methods, sales channels, and transaction dates.

## Tools Used
- Power BI Desktop
- Power Query
- DAX

## Data Cleaning
- Trimmed whitespace and cleaned text columns.
- Corrected numeric and date data types.
- Checked Transaction IDs for duplicates; none were found.
- Validated total spending against unit price multiplied by quantity.
- Recovered 609 missing unit prices using total spending divided by quantity.
- Retained missing values when there was insufficient information to calculate them.

## Dashboard Features
- Total Sales
- Total Transactions
- Average Transaction Value
- Sales by Category
- Sales by Payment Method
- Sales by Location: Online vs In-store
- Monthly Sales Trend
- Interactive date filter

## DAX Measures

```DAX
Total Sales =
SUM(Retail_Clean[Total Spent Clean])

Total Transactions =
COUNTROWS(Retail_Clean)

Average Transaction Value =
AVERAGE(Retail_Clean[Total Spent Clean])
```

## Key Findings
- Recorded sales totaled **1,552,071** across **12,575 transactions**.
- Average transaction value was **129.65**, calculated from transactions with available sales values.
- Butchers generated the highest category sales, while Milk Products generated the lowest.
- Online accounted for approximately **51%** of recorded sales, compared with **49%** for In-store.
- Cash generated the highest sales among the three payment methods.

## Data Limitations
- Sales values remain missing for **604 transactions**. These transactions are included in Total Transactions but excluded from Total Sales and Average Transaction Value.
- January 2025 includes data only through **18 January**, so its total is not directly comparable with a complete month.
- Monetary values are shown without a currency symbol because the currency has not been confirmed.

## Project Files
- [Power BI dashboard](Retail_Sales_Dashboard.pbix) — download and open in Power BI Desktop.
- [PDF preview](Retail_Sales_Dashboard.pdf) — static dashboard preview.

To refresh the Power BI file, update the CSV source path in Power Query to match the dataset location on your computer.
