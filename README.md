# 🚀 End-to-End Data Engineering Pipeline (Databricks | FMCG Domain)

![Python](https://img.shields.io/badge/Python-3.12-blue)
![PySpark](https://img.shields.io/badge/PySpark-Data%20Processing-orange)
![SQL](https://img.shields.io/badge/SQL-Analytics-green)
![Databricks](https://img.shields.io/badge/Databricks-Lakehouse-red)
![AWS](https://img.shields.io/badge/AWS-S3-yellow)
![Delta Lake](https://img.shields.io/badge/Delta-Lake-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Overview

This project demonstrates a **production-style end-to-end data engineering pipeline** built using **Databricks and AWS**, designed for an FMCG business scenario.

The pipeline integrates data from:
- 🏢 **Parent Company (Atlon)** – Structured enterprise data system  
- ⚡ **Child Company (Sports Bar)** – Unstructured, inconsistent data  

🎯 **Objective**:  
Create a **scalable and reliable data platform** that unifies data from both companies and enables **consistent analytics and reporting**.

---

## 🧠 Problem Statement

After acquiring a startup (Sports Bar), the parent company faced:

- Inconsistent data schemas  
- Missing and incomplete records  
- Data quality issues (duplicates, nulls, typos)  
- No unified reporting system  

💡 **Solution Approach**:
- Build a **data lake + lakehouse architecture**
- Clean and standardize raw data
- Create a **single source of truth (Gold layer)**

---

## 🏗️ Project Architecture

<p align="center">
  <img src="assets/project_architecture.png" alt="Project Architecture" width="900"/>
</p>

### 🔍 Architecture Explanation

The system follows a **modern Lakehouse architecture** using Databricks:

### 1️⃣ Data Ingestion Layer
- Raw data from **child company** is stored in **AWS S3**
- Data includes CSV files (customers, products, orders, pricing)

---

### 2️⃣ Processing Layer (Databricks)

#### 🟤 Bronze Layer (Raw Data)
- Stores raw ingested data from S3
- No transformation applied
- Adds metadata (file name, ingestion time)

---

#### ⚪ Silver Layer (Cleaned Data)
- Data cleaning & transformation:
  - Remove duplicates  
  - Handle null values  
  - Fix inconsistent formats  
  - Correct typos (e.g., "protin" → "protein")  
  - Standardize naming conventions  
- Apply business rules and mappings  

---

#### 🟡 Gold Layer (Business-Ready Data)
- Contains **analytics-ready tables**
- Structured using **star schema**
- Includes:
  - Dimension tables (Customers, Products, Date)
  - Fact table (Orders)

---

### 3️⃣ Data Integration Layer
- Merge **child company Gold data** into **parent Gold tables**
- Use **Delta Lake MERGE (Upsert)**:
  - Update existing records  
  - Insert new records  

---

### 4️⃣ Serving Layer
- Final Gold layer powers:
  - 📊 Dashboards  
  - 📈 Analytics  
  - 🤖 AI tools (Genie)

---

## 🔄 Data Pipeline

### Step-by-Step Workflow

1. **Extract**
   - Load CSV data into AWS S3

2. **Ingest**
   - Read data from S3 into Databricks Bronze layer

3. **Transform (Silver Layer)**
   - Clean data (duplicates, nulls, formatting)
   - Apply business logic

4. **Load (Gold Layer)**
   - Create analytics-ready tables

5. **Merge**
   - Combine child and parent datasets using upsert logic

6. **Serve**
   - Provide unified data for dashboards and reporting

---

## 🛠️ Tech Stack

| Category        | Tools / Technologies |
|----------------|--------------------|
| Language        | Python |
| Data Processing | PySpark |
| Query Language  | SQL |
| Platform        | Databricks |
| Storage         | AWS S3 |
| Data Format     | Delta Lake |
| Architecture    | Medallion (Bronze, Silver, Gold) |
| Orchestration   | Databricks Workflows |
| Visualization   | Databricks Dashboard |

---

## 🧹 Data Cleaning & Transformation

Key techniques applied:

- ✔ Duplicate removal  
- ✔ Null value handling  
- ✔ String normalization (trim, casing)  
- ✔ Regex-based corrections  
- ✔ Data standardization  
- ✔ Surrogate key generation (hashing)  
- ✔ Business rule mapping  

---

## 📂 Project Structure
```
data-engineering-project/
│
├── 1_setup/
│   ├── dim_date_table_creationg.ipynb
│   ├── setup_catalog.ipynb
│   └── utilities.ipynb
│
├── 2_dimension_data_processing/
│   ├── 1_customer_data_processing.ipynb
│   ├── 2_product_data_processing.ipynb
│   └── 3_pricing_data_processing.ipynb
│   
│
├── 3_fact_data_processing/
│   ├── 1_full_load_fact.ipynb
│   └── 2_incremental_load_f2act.ipynb
├── Dashboard/
│   ├── AtliQon BI 360.json
│   └── README.md
├── assets/
│   ├── dashboard-part1.png
│   ├── dashboard-part2.png
│   ├── dashboard-part3.png
│   └── project_architecture.png
│
└── README.md

```
---

## ⏱️ Data Processing Strategy

### 📦 Batch Processing
- Historical data (5 months)
- Backfilled into system

### ⚡ Incremental Processing
- Daily updates after deployment

---

## 🎯 Key Features

- 🔹 End-to-end pipeline using Databricks  
- 🔹 Scalable Lakehouse architecture  
- 🔹 Data quality handling (real-world scenarios)  
- 🔹 Delta Lake (ACID, time travel)  
- 🔹 Config-driven pipeline (flexible & reusable)  

---

## 🧑‍💻 Key Learnings

- Real-world data is messy and inconsistent  
- Data cleaning is the most critical step  
- Medallion architecture simplifies pipeline design  
- Delta Lake enables reliable data engineering  
- Business understanding is essential for transformations  

---

## 🚀 How to Run

1. Create a Databricks account  
2. Upload datasets to AWS S3  
3. Configure catalog & schemas  
4. Execute notebooks in order:
   - Setup  
   - Bronze  
   - Silver  
   - Gold  
5. Validate Gold tables  
6. Build dashboard  

---

## 📌 Conclusion

This project showcases:

- End-to-end data pipeline development  
- Real-world data transformation techniques  
- Scalable and production-ready architecture  

💼 **Ideal for**:
- Data Engineering portfolios  
- Resume projects  
- Interview discussions  

---

## ⭐ Support

If you found this project helpful:

- ⭐ Star the repository  
- 🍴 Fork it  
- 📢 Share with others  
