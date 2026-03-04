# 🚗 Car Sales Performance Analysis
### Capstone Project – Data Analysis with Python & Power BI  

---

# 📌 Project Overview

This project analyzes the **sales performance, customer behavior, and inventory efficiency** of an automotive dealership.

The goal of the analysis is to transform operational sales and inventory data into **strategic insights that support data-driven business decisions**.

The project uses:

- **Python** for data cleaning
- **Power BI** for building the interactive dashboard

---

# 🏠 Dashboard Home

![Home](images/0_home.png)

The dashboard home page acts as a **navigation hub**, allowing users to quickly access the different analytical sections of the project.

---

# 📊 Executive Overview

![Executive Overview](images/1_Executive%20Overview.png)

This section provides a high-level overview of the dealership’s overall performance.

Main KPIs:

- Total Revenue
- Revenue Growth
- Number of Customers
- Units Sold

It also includes the **monthly revenue trend** and the distribution of sales by brand.

---

# 🚘 Sales Performance Analysis

![Sales Analysis](images/2_Sales%20Analysis.png)

This page analyzes the main drivers of sales performance.

The analysis includes:

- revenue by brand
- sales distribution by engine type
- relationship between average price and units sold
- sales by price segment

This helps identify **which pricing strategies and brands generate the best performance**.

---

# 👥 Customer Insights

![Customer Insights](images/3_Customer%20Insights.png)

The Customer Insights section analyzes customer purchasing behavior.

It includes:

- revenue by age group
- sales by city
- top customers

This analysis helps identify **the most profitable customer segments**.

---

# 📅 Sales Trends Over Time

![Time Trends](images/4_Time%20Trends.png)

This section analyzes how sales evolve over time.

Main indicators include:

- Sales YTD
- Month-over-Month growth
- Year-over-Year growth

The chart allows us to identify **seasonal trends and variations in sales performance**.

---

# 📦 Model Performance & Stock Pressure

![Model Performance](images/5_Product%20&%20Stock%20Model.png)

This section analyzes the relationship between:

- model sales performance
- units sold
- available stock

A **Stock Pressure Index** was developed to evaluate the efficiency of inventory turnover.

---

# 📊 Strategic Insights

![Strategic Insights](images/6_Strategic%20Insights.png)

This chart compares:

- sales performance
- stock pressure

The scatter plot is divided into four quadrants that help identify:

- top performers
- growth opportunities
- critical stock areas

This analysis helps highlight **brands that may require strategic attention**.

---

# 📦 Product & Stock Analysis

![Product Stock](images/7_Product%20&%20Stock.png)

This page provides a deeper analysis of inventory management.

It includes:

- inventory value by brand
- units available in stock
- high stock risk
- model distribution by stock risk level

---

# 🎯 Strategic Recommendations

![Strategic Recommendations](images/8_Strategic%20Recommendations.png)

The final section translates analytical insights into **strategic recommendations**.

Suggested actions include:

- inventory rebalancing
- pricing strategy review
- continuous monitoring of the stock pressure index
- focusing on high-growth brands

- ---

# ⭐ Key Business Insights

The analysis revealed several important insights about sales performance and inventory management within the dealership:

### 📈 Strong Revenue Performance
The dealership shows strong overall revenue performance, with revenue concentrated across a small number of top-performing brands.

### 🚗 Premium Brands Drive Higher Revenue
Premium brands tend to generate higher revenue, supported by higher average selling prices and stable demand patterns.

### 📦 Inventory Pressure Is Not Even Across Brands
The Stock Pressure Index highlights that inventory pressure differs across brands and models, suggesting the need for targeted inventory monitoring.

### ⚠️ Potential Inventory Risk Areas
Some brands show high inventory pressure combined with strong sales performance, indicating a potential risk of inventory imbalance that should be monitored carefully.

### 🎯 Opportunities for Optimization
Brands with lower revenue performance but similar inventory pressure may benefit from pricing adjustments, promotional strategies, or improved inventory allocation.

---

# 🧹 Data Cleaning (Python)

The main data cleaning operations include:

- removing missing values
- converting data types
- cleaning price columns
- handling duplicates
- converting date columns

Example:

```python
import pandas as pd

df = pd.read_csv("sales.csv")

df = df.dropna()

df["Price"] = df["Price"].replace(r'[$,]', '', regex=True).astype(float)

df["Sale_Date"] = pd.to_datetime(df["Sale_Date"])

df = df.drop_duplicates()
