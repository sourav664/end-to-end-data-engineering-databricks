# 📊 Sales Insights Dashboard (Databricks)

## 📌 Overview

This dashboard provides **interactive sales insights** built on top of the **Gold Layer (analytics-ready data)** from the data engineering pipeline.

It enables business users to:
- Track revenue trends 📈  
- Analyze product performance 🏷️  
- Understand customer behavior 👥  
- Compare sales across channels and platforms  

---

## 🖥️ Dashboard Preview

### 🔹 Main Overview Dashboard

<p align="center">
  <img src="/assets/dashboard-part1.png" alt="Sales Dashboard Overview" width="1000"/>
</p>

### 🔹 Trends & Distribution Analysis

<p align="center">
  <img src="/assets/dashboard-part2.png" alt="Sales Trends Dashboard" width="1000"/>
</p>

### 🔹 Division-Level Performance

<p align="center">
  <img src="/assets/dashboard-part3.png" alt="Division Performance Dashboard" width="1000"/>
</p>

---

## 🎯 Key Features

### 📌 KPI Metrics
- Total Revenue  
- Total Quantity Sold  
- Unique Customers  
- Average Selling Price  
- Unique Divisions & Categories  

---

### 📊 Product Insights
- Top 10 products by revenue  
- Top variants by revenue  
- Category-wise performance  

---

### 📈 Time-Based Analysis
- Monthly revenue trends  
- Seasonal sales patterns  

---

### 🛒 Channel & Platform Analysis
- Revenue by channel (Retail, Direct, Acquisition)  
- Platform comparison:
  - Brick & Mortar  
  - E-Commerce  
  - Sports Bar  

---

### 👥 Customer Analysis
- Revenue by customer  
- Customer-level contribution  
- High-value customers identification  

---

### 🧩 Division Analysis
- Top divisions by revenue  
- Platform-wise contribution within each division  

---

## 🎛️ Interactive Filters

The dashboard includes dynamic filters for:

- Year  
- Quarter  
- Month  
- Channel  
- Category  

👉 Enables flexible, drill-down analysis  

---

## 🛠️ Tech Stack

| Component       | Tool Used |
|----------------|----------|
| Data Source     | Databricks Gold Layer |
| Processing      | PySpark |
| Querying        | SQL |
| Visualization   | Databricks Dashboard |
| Storage         | Delta Lake |

---

## 🔄 Data Flow
📥 Raw Data → 🟤 Bronze → ⚪ Silver → 🟡 Gold → 📊 Dashboard

- Data is cleaned and transformed in Silver  
- Aggregated and modeled in Gold  
- Dashboard consumes Gold tables  

---

## 💡 Business Impact

This dashboard helps stakeholders to:

- 📊 Make data-driven decisions  
- 📈 Identify high-performing products  
- 🛍️ Optimize sales channels  
- 👥 Understand customer segments  
- 📉 Detect trends and anomalies  

---


