# 📦 Apache Parquet

## What is Parquet?

**Parquet** is a **columnar storage file format** designed for **efficient data analytics and big-data processing**.

Instead of storing data row-by-row (like CSV or JSON), Parquet stores data **column-by-column**, making it faster and more storage-efficient for analytical queries.

---

## Row vs Column Storage

### Row-based (CSV / JSON)
1, Alice, 50000
2, Bob, 60000
- Reads entire rows
- Slow for analytics
- Larger file size

### Column-based (Parquet)
id → 1, 2
name → Alice, Bob
salary → 50000, 60000

- Reads only required columns
- Faster queries
- Better compression

---

## Why Use Parquet?

### 🚀 Performance
- Reads only selected columns
- Faster `SELECT`, `WHERE`, `GROUP BY`

### Write
```python
df.write.parquet("employees.parquet")
spark.read.parquet("employees.parquet")

## 📄 CSV (Comma-Separated Values)

CSV is a **row-based, plain text** file format.

### Example
```csv
id,name,salary
1,Alice,50000
2,Bob,60000
```

## 📄 JSON (JavaScript Object Notation)

JSON is a **lightweight, semi-structured, row-based** data format commonly used for **APIs, configuration files, and logs**.

### Example

```json
[
  {
    "id": 1,
    "name": "Alice",
    "salary": 50000
  },
  {
    "id": 2,
    "name": "Bob",
    "salary": 60000
  }
]
```
