# ⚙️ OLTP – Online Transaction Processing

## 1️⃣ What is OLTP?

**OLTP (Online Transaction Processing)** refers to systems that handle **day-to-day application transactions** in real time.

## 2️⃣What Kind of Operations Does OLTP Handle?

OLTP focuses on:
- INSERT
- UPDATE
- DELETE
- Simple SELECT (single or few rows)

✔ Small transactions  
✔ Very frequent  
✔ Fast execution (milliseconds)

---

## 3️⃣ OLTP Example (Real Application)

### E-commerce Application

User actions:
- Login
- Add item to cart
- Place order
- Make payment

Each action triggers an **OLTP transaction**.

```sql
BEGIN;
INSERT INTO orders VALUES (101, 1, 999);
UPDATE inventory SET stock = stock - 1 WHERE product_id = 10;
COMMIT;
```
## 🗄️ Common Databases Used for OLTP

OLTP systems commonly use the following databases to handle real-time transactional workloads:

- **MySQL**
- **PostgreSQL**
- **Oracle**
- **SQL Server**
- **MongoDB**

These databases act as **OLTP systems** when used for frequent `INSERT`, `UPDATE`, `DELETE`, and fast read operations.

## ❌ What OLTP Is NOT Used For

OLTP systems are **not designed for heavy analytical workloads**.

❌ Heavy aggregations  
❌ Large table scans  
❌ Complex reporting queries  

### Example of a Query NOT Suitable for OLTP

```sql
SELECT country, SUM(amount)
FROM orders
GROUP BY country;
```
# ❌ OLTP Is Not Meant for Heavy Aggregations

OLTP systems are designed for **fast, real-time transactions**, not analytical workloads.

---

## 🚫 Why Heavy Aggregation Queries Are Not Suitable for OLTP

Running heavy analytical queries on an OLTP database can:

- Slow down live applications
- Increase response time for users
- Impact transaction performance

---

## ❗ Example of a Heavy Aggregation Query

```sql
SELECT country, SUM(amount)
FROM orders
GROUP BY country;
