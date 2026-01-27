# 🗄️ Database – Step-by-Step (Beginner Friendly)

## 1️⃣ What is a Database?

A **database** is a place where an application **stores and manages data needed for daily operations**.

---

## 2️⃣ Why Do We Need a Database?

Applications must store data such as:
- User details
- Login credentials
- Orders
- Payments
- Transactions

A database ensures:
- Data is stored safely
- Data can be updated frequently
- Data can be accessed very fast

---

## 3️⃣ What Kind of Work Does a Database Do?

Databases are designed for **OLTP workloads**.

### OLTP – Online Transaction Processing
- Many users at the same time
- Very frequent INSERT, UPDATE, DELETE
- Small and fast transactions
- Real-time operations

Example:
```sql

INSERT INTO orders VALUES (101, 'Phone', 999);
UPDATE orders SET price = 899 WHERE id = 101;
```

# 🔑 Primary Key

### ✅ What is a Primary Key?

A **Primary Key** uniquely identifies **each row** in a table.

### 📌 Rules of Primary Key
- Must be **unique**
- Cannot be **NULL**
- Only **one** primary key per table

---

### 🔹 Example: Primary Key

```sql
CREATE TABLE users (
  user_id INT PRIMARY KEY,
  name VARCHAR(50),
  email VARCHAR(100)
);
```
# 🔗 Foreign Key

## 1️⃣ What is a Foreign Key?

A **Foreign Key (FK)** is a column (or group of columns) in one table that **refers to the Primary Key of another table**.

> A foreign key creates a **relationship between two tables**.
