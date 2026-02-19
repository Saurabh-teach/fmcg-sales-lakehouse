# 🚀 FMCG Sales Lakehouse – End-to-End Data Engineering Pipeline

## 📌 Overview
This project implements a complete Lakehouse architecture using Databricks and Delta Lake for processing FMCG sales data.  
It follows the Medallion Architecture (Bronze → Silver → Gold) and builds a Star Schema to power executive dashboards.

---

## 🏗 Architecture
<img width="20005" height="11129" alt="project_architecture" src="https://github.com/user-attachments/assets/11d31d86-f1b2-4e30-9f9e-65d181cea6db" />


### 🔹 Bronze
- Raw CSV ingestion from S3 / Unity Catalog
- Append-only Delta tables
- Metadata tracking

### 🔹 Silver
- Data cleansing & validation
- Deduplication
- Incremental MERGE logic
- Business rule enforcement

### 🔹 Gold
- Star Schema modeling
- Fact table: `fact_orders`
- Dimension tables:
  - `dim_products`
  - `dim_customers`
  - `dim_gross_price`
  - `dim_date`
- Monthly aggregation logic

### 🔹 Analytics Layer
Denormalized reporting view:

