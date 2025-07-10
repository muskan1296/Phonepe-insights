# Phonepe-insights
# PhonePe Pulse ETL Pipeline

A Python-based end-to-end pipeline that clones the PhonePe Pulse repository, extracts JSON data, cleans & enriches it, then loads everything into a MySQL database for easy analysis.

---

## 🔍 Overview
- **Goal:** Automate ingestion of nested JSON files (transactions, users, maps, top districts/pincodes) into structured MySQL tables  
- **Why:**  
  - Centralize data for SQL querying  
  - Power BI/Tableau dashboards or custom analytics  
  - Easily extend with new JSON dumps

---

## 🚀 Features

- Automated `git clone` with GitPython  
- Recursive directory traversal to discover all JSON categories  
- Pandas-powered DataFrames for loading & cleaning  
- Geographic enrichment (state/region, lat/long)  
- CSV export for portability  
- Parameterized bulk `INSERT` into MySQL  
- Verification of row counts to ensure data integrity

---

## ⚙️ Prerequisites

- Python 3.8+  
- MySQL 5.7+ (or compatible)  
- Git  
- Python packages:
  ```bash
  pip install gitpython pandas mysql-connector-python
