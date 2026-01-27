# 📊 OLAP – Online Analytical Processing 

## 1️⃣ What is OLAP?

**OLAP (Online Analytical Processing)** is used for **data analysis and reporting**.

> OLAP helps answer questions like  
> “What happened in the business?”

---

##2️⃣ What Kind of Questions Does OLAP Answer?

OLAP answers **business questions** like:

- Total sales by country?
- Revenue by year?
- Top-selling products?
- Monthly growth trends?

Example:
```sql
SELECT country, SUM(revenue)
FROM sales
GROUP BY country;
```
## 5️⃣ OLAP Operations (Core Concepts)

OLAP supports the following operations:

### 🔹 Aggregation

```sql
SUM(), COUNT(), AVG(), MIN(), MAX()
```

### 🔹 Grouping & Filtering

```sql
GROUP BY year, region
```

```sql
WHERE year BETWEEN 2020 AND 2024
```





