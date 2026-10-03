# E-Commerce Sales Data Analysis

## Project Overview

This project focuses on analyzing an e-commerce sales dataset to understand
sales performance, profitability, customer payment behavior, product
performance, and monthly business trends.

The project includes data cleaning, exploratory data analysis (EDA),
visualization, KPI calculation, and business insights.

## Business Objectives

- Analyze overall sales and profit performance
- Identify high-performing categories and products
- Analyze city-wise sales
- Understand payment mode usage
- Identify monthly sales and profit trends
- Analyze the relationship between sales and profit
- Calculate key business KPIs
- Identify and handle data quality issues

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- VS Code
- Git & GitHub



## Dataset

The dataset contains e-commerce transaction-level data with the following columns:

- Order_ID
- Order_Date
- Customer_Name
- Category
- Product
- Quantity
- Sales
- Profit
- City
- Payment_Mode

The dataset contains intentional data quality issues such as missing values,
duplicate Order_IDs, negative sales values, and potential outliers.

## Data Cleaning

The following data cleaning steps were performed:

1. Identified missing values using `isnull().sum()`.
2. Filled missing customer names with `"Unknown"`.
3. Filled missing categories using product-based category information.
4. Filled missing products with `"Unknown"` where the exact product could not
   be reliably determined.
5. Filled missing Quantity values using the median.
6. Filled missing Sales and Profit values using product-wise median values.
7. Identified duplicate transactions using `Order_ID`.
8. Removed duplicate Order_ID records while keeping the first occurrence.
9. Converted `Order_Date` from string format to datetime format.
10. Identified negative Sales values and removed invalid transactions.
11. Investigated Profit outliers using the IQR method.
12. Retained high-profit observations after investigation because they were
    associated with high Sales and Quantity values.


## Exploratory Data Analysis (EDA)

The following analyses were performed:

### Category Analysis
- Calculated total Sales by Category
- Calculated total Profit by Category
- Calculated average Profit by Category

### Product Analysis
- Calculated total Sales by Product
- Identified Top 10 Products by Sales
- Identified Top 10 Products by Profit

### City Analysis
- Calculated total Sales by City

### Payment Analysis
- Analyzed order distribution by Payment Mode

### Monthly Analysis
- Calculated monthly Sales
- Calculated monthly Profit
- Analyzed monthly Sales and Profit trends

### Relationship Analysis
- Calculated the correlation between Sales and Profit
- Created a scatter plot to visualize the relationship

## Key Performance Indicators (KPIs)

The following KPIs were calculated:

- Total Sales
- Total Profit
- Total Orders
- Average Order Value (AOV)
- Total Quantity Sold
- Profit Margin %

## Key Business Insights

- Electronics generated the highest total Sales and total Profit among all categories.
- Smartphone was the highest-selling product based on total Sales.
- Mumbai recorded the highest total Sales among the analyzed cities.
- December recorded the highest monthly Sales and monthly Profit.
- Net Banking was the most frequently used Payment Mode, with 182 orders.
- Sales and Profit showed a strong positive correlation of approximately 0.91.
- Potential Profit outliers were investigated using the IQR method instead of being removed automatically.


## Visualizations

The following visualizations were created using Matplotlib:

1. Total Sales by Category
2. Total Profit by Category
3. Total Sales by Product
4. Total Sales by City
5. Orders by Payment Mode
6. Monthly Sales Trend
7. Monthly Profit Trend
8. Sales vs Profit Scatter Plot
9. Top 10 Products by Sales
10. Top 10 Products by Profit



## Conclusion

This project demonstrates an end-to-end data analysis workflow using Python.

The analysis covered data cleaning, exploratory data analysis, visualization,
KPI calculation, and business insight generation.

The project helped identify category, product, city, payment, and monthly
performance patterns while also demonstrating how to handle common data
quality issues such as missing values, duplicates, invalid values, and
potential outliers.

## Project Structure

```text
Ecommerce-Sales-Analysis/
│
├── ├── Data/
│   ├── ecommerce_sales_raw.csv
│   └── salas_analysis.ipynb
│
├── Notebook/
│   └── ecommerce_sales_analysis.ipynb
│
├── README.md
│
└── requirements.txt