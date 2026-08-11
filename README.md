# Chocolate Sales in Power BI Dashboard

Hello and welcome to my Power BI dashboard!

I built an interactive Power BI dashboard analyzing chocolate retail sales across countries, brands, and products (2023–2024). I built this as a portfolio project to practice my Power BI skills end-to-end: data modeling, DAX, and dashboard design.

![Executive Overview](images/executive_overview.jpg)

## Objective

I did this dashboard to practice Power BI beyond just writing measures. I wanted to focus on **UX and visual design**: consistent color palette, clear navigation, drill-through, and dynamic visuals that respond to user selections.

The dashboard was designed for **sales/business managers** who want a periodic (not real-time) view of performance:
- Compare revenue, profit, and orders year-over-year
- Spot top/underperforming countries, brands, and products
- Identify seasonal patterns to plan promotions and stock
- Drill down from a country/brand overview into product-level detail without leaving the flow


## Data Source

[Chocolate Sales Dataset (2023–2024) — Kaggle](https://www.kaggle.com/datasets/ssssws/chocolate-sales-dataset-2023-2024)

Synthetic FMCG-style retail data with a **star schema**: a `Sales` fact table connected to `Products`, `Stores`, `Customers`, and `Calendar` dimension tables.


## 🖥️ Dashboard Pages

**1. Executive Overview**
KPI cards (Profit, Revenue, Orders, Units Sold, AOV) with YoY comparison, revenue/profit trend, revenue by country (with flag images), revenue by brand and store type, and a top 10 products table.
Plus a **Detail by Brand** drill-through page for row-level product data by brand.

**2. Product Performance**
Country-level deep dive with a flag image that updates dynamically based on the selected country, profit/revenue by category and brand, cocoa % breakdown, and a full product ranking table. A metric selector (Profit/Revenue) lets the user switch KPIs **without triggering a full cross-filter** on every chart — some visuals stay fixed for stable comparison.

**3. Time Intelligence & Seasonality**
Year-over-year and quarter-over-quarter revenue/profit table, a quarter/month treemap, and revenue by day of the week to surface seasonality patterns.

## ⚙️ Key Elements & Techniques

- **Star schema** data model (Sales fact + Products, Stores, Customers, Calendar dimensions)
- **DAX measures** for dynamic KPI card coloring (background + text color change based on YoY performance)
- **DAX-driven treemap coloring** by quarter
- **Quick measures** for time intelligence (YoY, QoQ)
- **Drill-through** from Executive Overview into brand-level detail
- **Selective cross-filtering**: metric selector on Product Performance changes some visuals while others stay fixed, for controlled comparison
- **Dynamic image**: country flag updates based on slicer/filter selection
- **Custom navigation panel** with buttons across all pages
- **Segmented filter panel** (Year, Country, Category, Store Type) for a cleaner, organized sidebar
- Consistent chocolate-themed color palette and typography throughout

## Tools

Power BI Desktop · DAX · Power Query

## Repo Contents

- `chocolate_sales.pbix` — Power BI file
- `/images` — dashboard screenshots

---

## About Me

Hi there! I’m **Valeria Yagui**, from Lima, Peru.  
I'm currently pursuing a **Master’s degree in Digital Business Management** at **Hochschule Pforzheim** in Germany.  
I enjoy working with data and learning new tools and technologies.  

Feel free to connect with me on LinkedIn:  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/valeria-yagui-nishii/)
