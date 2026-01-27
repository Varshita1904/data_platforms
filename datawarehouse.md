# 🏭 Data Warehouse

## 1️⃣ What is a Data Warehouse?

A **Data Warehouse** is a centralized system used to **store historical data** for **analysis and reporting**.

> A data warehouse answers the question:  
> **“What happened in the business over time?”**

---

## 2️⃣ Why Do We Need a Data Warehouse?

Operational databases (OLTP) are built to:
- Run applications
- Handle transactions

They are **not suitable** for analytics.

A Data Warehouse:
- Separates analytics from live systems
- Stores large volumes of historical data
- Supports OLAP queries efficiently

---

## 3️⃣ What Kind of Work Does a Data Warehouse Do?

Data Warehouses are designed for **OLAP workloads**.

They handle:
- Large SELECT queries
- GROUP BY
- Aggregations (SUM, COUNT, AVG)
- Joins across many tables

## 📦 Data Stored in a Data Warehouse

A Data Warehouse stores **analysis-ready data**, not raw or transactional data.

### Types of Data Stored:
- **Structured data** (tables with rows and columns)
- **Historical data** (data over months or years)
- **Aggregated data** (daily, monthly, yearly summaries)
- **Cleaned & transformed data**
- **Semi-structured data** (JSON, XML – in modern warehouses)

### Not Stored:
- Raw logs
- Images, videos, audio
- streaming data
- Frequently changing data

> **Data Warehouse = clean, structured, historical data for analytics**

Example:
```sql
SELECT region, SUM(revenue)
FROM sales
GROUP BY region;
```
