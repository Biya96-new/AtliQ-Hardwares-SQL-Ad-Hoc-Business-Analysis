# 📊 AtliQ Hardwares – SQL Ad-Hoc Business Analysis

## 🧾 Overview

This project focuses on solving real-world **ad-hoc business requests** for AtliQ Hardwares using SQL.  
The goal is to extract meaningful insights from raw transactional data to support **data-driven decision-making** across markets, customers, products, and sales channels.

---

## 🎯 Problem Statement

AtliQ Hardwares generates large volumes of sales, product, and customer data across multiple regions. However, the business faced a key challenge:

- Lack of a structured system to analyze ad-hoc business questions  
- Dependence on manual or fragmented reporting  
- Limited access to fast, data-driven insights for decision-making  

Because of this, stakeholders struggled to quickly understand performance across customers, products, and markets.

### 💡 Objective

This project aims to:

- Solve ad-hoc business questions using SQL  
- Transform raw data into structured insights  
- Analyze trends in sales, customers, products, and pricing  
- Enable faster and better business decision-making  

---

## 🏢 About AtliQ Hardwares

AtliQ Hardwares is a global computer hardware manufacturer with presence in:

- Asia Pacific  
- Europe  
- North America  
- Latin America  

### Business Segments:
- Personal Computing  
- Peripherals & Accessories  
- Networking & Storage  

---

## 🗃️ Dataset Overview

### Dimension Tables
- `dim_customer` → Customer details, market, region, channel  
- `dim_product` → Product details, segment, division, category  

### Fact Tables
- `fact_sales_monthly` → Monthly sales transactions  
- `fact_gross_price` → Product pricing details  
- `fact_manufacturing_cost` → Manufacturing cost data  
- `fact_pre_invoice_deductions` → Discount information  

---

## 🛠️ Tools & SQL Techniques Used

- Joins (INNER JOIN, LEFT JOIN)
- Aggregations (SUM, COUNT, AVG)
- Common Table Expressions (CTEs)
- Window Functions (DENSE_RANK, RANK)
- Subqueries
- CASE WHEN Statements
- Date Functions (MONTH, YEAR, MONTHNAME)
- Grouping & Sorting

---

## 🧹 Data Cleaning

```sql
SET SQL_SAFE_UPDATES = 0;

UPDATE dim_customer
SET market = 'Philippines'
WHERE market = 'Philiphines';

UPDATE dim_customer
SET market = 'New Zealand'
WHERE market = 'Newzealand';
