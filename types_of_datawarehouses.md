## 🏭 Popular Data Warehouses & Their SQL Syntaxes (Latest)

Below are **3 widely used modern data warehouses** and the **common SQL syntaxes** they support.

---

## 1️⃣ Snowflake

**Type:** Cloud-native data warehouse  
**SQL Style:** ANSI SQL (Snowflake SQL)
**Snowflake** = data warehouse that runs on AWS / Azure / GCP
### Common Syntax Examples

```sql
CREATE TABLE customers (
  id INT,
  name STRING,
  country STRING
)
```
-- Load data
```sql
COPY INTO customers
FROM @my_stage/customers.csv
FILE_FORMAT = (TYPE = CSV);
```
-- Query
```sql
SELECT country, COUNT(*)
FROM customers
GROUP BY country;
```

## Common Data Sources
- **Databases** (MySQL, PostgreSQL, Oracle)
- **Files** (CSV, JSON, Parquet)
- **Data Lakes** (AWS S3, Azure ADLS, GCP GCS)

## 2️⃣ Google BigQuery

**Type:** Serverless cloud data warehouse  
**SQL Style:** Standard SQL (BigQuery SQL)  

**BigQuery** is a fully managed, serverless data warehouse provided by **Google Cloud Platform (GCP)**.

---

### Common BigQuery SQL Syntax

#### Create Table
```sql
CREATE TABLE my_project.sales.customers (
  id INT64,
  name STRING,
  country STRING
);
```
### Common Data Sources for BigQuery

- **Databases**: MySQL, PostgreSQL  
- **Files**: CSV, JSON, Parquet  
- **Data Lakes**: Google Cloud Storage (GCS)  
- **Streaming Data**: via Pub/Sub  

## 📥 How Data Is Loaded into BigQuery

BigQuery does **not** receive data directly from users or applications.  
Data is loaded **after it is generated**.

---

## 1️⃣ Common Ways to Load Data into BigQuery

### ✅ 1. From Files (Most Common)
Data is loaded from files stored in **Google Cloud Storage (GCS)**.

**Supported formats:**
- CSV
- JSON
- Parquet
- Avro

**Flow:**

---

### ✅ 2. From Databases (Batch Load)
Data is copied from:
- MySQL
- PostgreSQL
- Other OLTP databases

Usually done using **ETL / ELT tools**.

**Flow:**

---

### ✅ 3. Streaming Data (Near Real-Time)
BigQuery can receive streaming data using:
- Pub/Sub
- APIs

Used when data needs to be available quickly for analysis.

---

# 🏭 Amazon Redshift – Data Warehouse 

## What is Amazon Redshift?

**:contentReference[oaicite:0]{index=0}** is a **cloud-based data warehouse** provided by **AWS** for **analytical (OLAP) workloads**.

> Redshift is used to analyze large amounts of data using SQL.

---

### SQL-Based (PostgreSQL Style)
- Uses PostgreSQL-like SQL
- Easy for SQL users to learn

---

### 1️⃣ Strong AWS Integration
Works seamlessly with:
- Amazon S3
- AWS Glue
- IAM
- Lambda

Best choice for **AWS-based architectures**.

---

### 2️⃣ Columnar Storage
- Data stored by **columns**
- Faster aggregations
- Efficient large data scans

---

| Feature | Snowflake | BigQuery | Amazon Redshift |
|------|----------|---------|----------------|
| Provider | :contentReference[oaicite:0]{index=0} | :contentReference[oaicite:1]{index=1} | :contentReference[oaicite:2]{index=2} |
| Cloud | AWS, Azure, GCP | GCP only | AWS only |
| Type | Fully managed | Serverless | Managed (cluster-based) |
| SQL Style | ANSI SQL | Standard SQL | PostgreSQL-like SQL |



