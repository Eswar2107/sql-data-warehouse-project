# SQL Data Warehouse Project – Medallion Architecture

## 📌 Project Overview
This project demonstrates the implementation of a **SQL Server Data Warehouse** using the **Medallion Architecture (Bronze, Silver, Gold layers)**.  
The data was sourced from multiple **CSV files**, ingested into SQL Server, cleaned and transformed, and finally modeled for analytics and reporting.

The goal of this project is to showcase **data engineering best practices**, including structured data ingestion, transformation, and dimensional modeling.

---

## 🏗️ Architecture Overview
The warehouse follows the **Medallion Architecture**, which organizes data into three logical layers:


---

## 🥉 Bronze Layer (Raw Data)

### Purpose
- Store raw data exactly as received from CSV files  
- Minimal or no transformation  

### Details
- Data is ingested directly from CSV files into SQL Server tables  
- Maintains original schema and values  
- Serves as the single source of truth  

### Example Tables
- `bronze.crm_cust_info`
- `bronze.crm_prd_info`
- `bronze.crm_sales_details`
- `bronze.erp_cust_az12`
- `bronze.erp_loc_a101`
- `bronze.erp_px_cat_g1v2`

---

## 🥈 Silver Layer (Cleaned & Transformed Data)

### Purpose
- Clean, standardize, and transform raw data  
- Prepare data for analytics  

### Transformations Performed
- Removed duplicates  
- Handled null and invalid values  
- Standardized column formats  
- Applied business rules  
- Data type corrections  

### Example Tables
- `silver.crm_cust_info`
- `silver.crm_prd_info`
- `silver.crm_sales_details`
- `silver.erp_cust_az12`
- `silver.erp_loc_a101`
- `silver.erp_px_cat_g1v2`

---

## 🥇 Gold Layer (Business-Ready Data)

### Purpose
- Provide analytics-ready data  
- Support reporting and BI tools  

### Implementation
- Created **SQL Views**  
- Modeled using **fact and dimension design**  

### Gold Views
- `gold.dim_customers` – Customer dimension  
- `gold.dim_products` – Product dimension  
- `gold.fact_sales` – Sales fact table  

These views combine and enrich data from the Silver layer, making them suitable for dashboards and analytical queries.

---

## 🧰 Tools & Technologies
- SQL Server Express  
- SQL Server Management Studio (SSMS)  
- CSV Files (Source data)  
- T-SQL  
- Medallion Architecture  

---

## 📊 Data Modeling
- **Fact Table:** Sales transactions  
- **Dimension Tables:** Customers, Products  
- Designed for scalability and analytics performance  

---

## 🚀 Key Learnings
- Implementing a layered data warehouse architecture  
- Data ingestion from flat files into SQL Server  
- Data cleaning and transformation using T-SQL  
- Creating business-friendly views for analytics  
- Applying dimensional modeling concepts  
