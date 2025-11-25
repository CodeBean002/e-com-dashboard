# 📊 Global Sales Performance Analysis Dashboard (Power BI)

This project analyzes sales data to monitor key performance indicators (KPIs), identify geographical and product trends, and derive actionable business insights for strategic planning.

## 🚀 Project Overview

This repository contains the files and assets related to a comprehensive Sales Analysis project developed using **Microsoft Power BI**. The core objective was to transform raw transaction data into a dynamic, interactive dashboard that measures performance against the previous year (PY) and highlights high-impact areas for decision-making.

The project was inspired by the work of **Freedom Oboh**.

## ✨ Key Findings & Business Insights

The analysis uncovered several crucial points for the business:

| KPI | Value | YoY Change | Insight |
| :--- | :--- | :--- | :--- |
| **Total Revenue** | $105M | **+16.1%** | Strong revenue growth, driven by volume. |
| **Quantity Sold** | 6M | **+16.1%** | Growth is volume-based (Avg Price remained flat). |
| **Customer Concentration** | (High) | 0.0% (Customer Count) | Top Spenders are highly concentrated, posing a stability risk that requires immediate retention strategies. |
| **Top Product** | Cans | N/A | Cans are the dominant product by quantity, making them the benchmark for successful sales tactics. |

## 🛠️ Tools and Technologies

* **Primary Tool:** Microsoft Power BI Desktop
* **Data Modeling:** Star Schema Design
* **Calculations:** Data Analysis Expressions (DAX) for Year-over-Year (YoY) comparisons, aggregation, and custom measures.
* **Visualization:** Various charts including line charts for trends, donut charts for customer insight, and a Map visual for geographical distribution.

## ⚙️ Data Model (Star Schema)

The dashboard is built on a robust Star Schema model for optimal query performance and measure accuracy.

* **Fact Table:** `fact_table` (contains `item_key`, `store_key`, `time_key`, `coustomer_key`, and transaction details).
* **Dimension Tables:**
    * `customer_dim`
    * `item_dim`
    * `store_dim`
    * `time_dim`
    * `Trans_dim` (Payment/Transaction details)


## 📊 Dashboard Visuals

The dashboard provides a single, cohesive view of the business performance:

### 1. Performance Metrics
* Revenue, Quantity, and Avg Unit Price with YoY comparison.
* Monthly Sales Trend to identify seasonality and performance fluctuations.

### 2. Customer and Product Deep Dive
* **Customer Insight:** Top 5 Spenders analysis to highlight revenue concentration.
* **Top 5 Units by Quantity Sold:** Bar chart identifying the highest-volume products (e.g., Cans, Bottles).

### 3. Geographical Analysis
* Map visual showing sales distribution by country, reinforced by a Top 5 countries bar chart (e.g., Bangladesh, India, Lithuania).


## 📈 Key DAX Measures Used

* **Revenue:** `SUMX(fact_table, fact_table[Unit Price] * fact_table[Quantity])` (Example)
* **Previous Year (PY) Measures:** Used `CALCULATE()` with `SAMEPERIODLASTYEAR()` to enable accurate YoY comparisons.
* **YoY % Growth:** Used division of difference between current and PY Revenue by PY Revenue.

---
**Author:** EniolaNimi
