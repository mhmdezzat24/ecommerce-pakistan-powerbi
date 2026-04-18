# 🛍️ Pakistan E-Commerce Sales Insights

> **Power BI dashboard** analyzing Pakistan's largest e-commerce dataset

![Power BI](https://img.shields.io/badge/Tool-Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)

---

## 📌 Project Overview

This project analyzes **Pakistan's Largest E-Commerce Dataset** — a massive 100MB+ dataset covering hundreds of thousands of transactions. The goal was to build an interactive Power BI report that reveals key business insights around revenue trends, product category performance, payment methods, and customer behavior.

---

## 🎯 Objectives

- Analyze order status distribution (completed vs. canceled)
- Identify top-performing product categories
- Understand payment method preferences (COD vs. online)
- Track revenue trends across fiscal years
- Segment customers and revenue by key dimensions

---

## 📂 Dataset

| Column | Description |
|--------|-------------|
| item_id | Unique item identifier |
| status | Order status (complete / canceled / refund) |
| created_at | Order creation date |
| price | Item price |
| qty_ordered | Quantity ordered |
| grand_total | Total order value |
| category_name_1 | Product category |
| payment_method | COD / credit card / etc. |
| BI Status | Business intelligence classification |
| Year / Month / FY | Time dimensions |
| Customer ID | Unique customer identifier |

**Size:** 100MB+ | **Period:** FY2017 onwards

---

## 🔧 What Was Done

### Data Preparation
- Imported large CSV into Power BI
- Cleaned column types and handled null values
- Created calculated columns for fiscal year grouping
- Filtered out irrelevant/corrupted rows

### DAX Measures Created
```dax
Total Revenue = SUM(Sales[grand_total])
Completed Orders = CALCULATE(COUNTROWS(Sales), Sales[status] = "complete")
Cancellation Rate = DIVIDE([Canceled Orders], [Total Orders])
Avg Order Value = AVERAGE(Sales[grand_total])
```

### Visualizations Built

| Visual | Purpose |
|--------|---------|
| KPI Cards | Total Revenue · Avg Order Value · Total Orders |
| Bar Chart | Revenue by Product Category |
| Pie Chart | Order Status Distribution |
| Column Chart | Revenue by Payment Method |
| Line Chart | Revenue Trend by Month/Year |
| Table | Top Products by Revenue |

---

## 📊 Key Findings

- 🛒 **Women's Fashion** is the top-selling category by volume
- 💳 **Cash on Delivery (COD)** is the dominant payment method
- ❌ Significant **cancellation rate** — opportunity for operational improvement
- 📅 **FY2017** shows strong baseline; growth visible in subsequent years
- 💰 High-value orders tend to cluster in **Electronics** and **Fashion**

---

## 📁 Files in This Repository

```
ecommerce-pakistan-powerbi/
│
├── README.md
├── data/
│   └── Pakistan Largest Ecommerce Dataset.csv    # Raw dataset
└── E-commerce Sales Insights(EZZAT).pbix         # Power BI report
```

---

## 🚀 How to Open

1. Download `E-commerce Sales Insights(EZZAT).pbix`
2. Open in **Power BI Desktop** (free download from Microsoft)
3. Explore the interactive visuals using slicers and filters

---

## 👤 Author

**Mohamed Ezzat Anwar** — Data Analyst  
📧 mhmdezzat24@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/mohamedezzat222/)
