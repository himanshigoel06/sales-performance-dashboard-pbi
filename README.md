# 📊 Sales Performance Dashboard – Power BI Project

<p align="center">
  <img src="images/logo.png" width="120">
</p>

## 🚀 Project Overview

The **Sales Performance Dashboard** is an interactive business intelligence solution built using Power BI.  

It provides detailed insights into:

- Sales performance
- Profit trends
- Year-over-Year growth
- Regional and category analysis
- Top performing and loss-making sub-categories

This dashboard helps stakeholders make data-driven decisions efficiently.

---

## 🎯 Business Objectives

✔ Analyze overall sales and profitability  
✔ Identify top 5 performing sub-categories  
✔ Track Year-over-Year (YoY) growth  
✔ Monitor regional performance  
✔ Detect negative profit areas  
✔ Enable interactive filtering  

---

## 🛠 Tools & Technologies Used

- Power BI
- DAX (Data Analysis Expressions)
- Data Modeling
- Interactive Visualizations
- Business Intelligence Design Principles

---

## 📂 Data Source

Dataset: Sample Superstore Dataset  

Source URL:  
https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

---

## 📊 Key KPIs Implemented

- 💰 Total Sales  
- 📈 Total Profit  
- 📦 Total Orders  
- 📊 Profit Margin %  
- 📉 YoY Growth %  
- 🎯 Achievement % (KPI Indicator)  

---

## 🧠 DAX Measures Used

```DAX
Total Sales = SUM(Sales[Sales])

Total Profit = SUM(Sales[Profit])

Total Orders = COUNT(Sales[Order ID])

Profit Margin % = 
DIVIDE([Total Profit], [Total Sales])

Sales LY = 
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(Sales[Order Date])
)

YoY Growth % =
DIVIDE([Total Sales] - [Sales LY], [Sales LY])

Sales Target = 600000

Achievement % =
DIVIDE([Total Sales], [Sales Target])

Screenshot : https://github.com/himanshigoel06/sales-performance-dashboard-pbi/blob/main/SalesPerformance.png
