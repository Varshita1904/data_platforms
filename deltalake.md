# ⚡ Delta Lake

**Delta Lake** is a storage layer that adds **reliability and ACID transactions** to a Data Lake.

## Why Delta Lake Exists
Plain Data Lakes:
- No ACID guarantees
- Hard to update or delete data
- Risk of corrupted data

Delta Lake fixes these problems.

---

## Key Features
- ACID transactions
- Schema enforcement
- Time travel (query old versions)
- Reliable UPDATE / DELETE / MERGE
- Built on Data Lake storage

---

## Where Delta Lake Lives
- AWS S3
- Azure Data Lake Storage (ADLS)
- Google Cloud Storage (GCS)

---

# 📍 Where Is Delta Lake?

Delta Lake lives **on top of a Data Lake**, not as a separate system.

## Where It Physically Lives
- AWS S3
- Azure Data Lake Storage (ADLS)
- Google Cloud Storage (GCS)

## What It Is
- A storage layer on cloud object storage
- Not a database
- Not a server

## What Makes It Delta Lake
- Parquet data files
- `_delta_log` folder (transaction log)


