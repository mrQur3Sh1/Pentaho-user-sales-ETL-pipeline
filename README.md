# 🍕 Pentaho ETL Pizza Sales Pipeline

A complete data engineering pipeline built in **Pentaho Data Integration (Spoon)** that demonstrates real-world ETL processes — from raw CSV and JSON ingestion to PostgreSQL aggregation and reporting.

---

## 🔧 Tools & Technologies
- **Pentaho Spoon** (ETL)
- **PostgreSQL** (Database - NeonDB Cloud)
- **Kaggle Dataset** (Pizza Sales)
- JSON & CSV file parsing
- Job Orchestration & SQL Scripting

---

## 🧠 Project Overview

This ETL pipeline processes and analyzes restaurant pizza sales and customer data through multiple transformations, cleans the data, aggregates it, and loads it into a cloud-based database.

### 📥 **Extract**
- Imported Pizza Sales from `User_pizza_sales.csv` (Kaggle)
- Loaded User Info from a JSON structure

### 🔄 **Transform**
- **Transformation 1**:  
  - Extract CSV  
  - Clean & select fields  
  - Load into `restaurant_sales` table

- **Transformation 2**:  
  - Parse JSON  
  - Extract user info  
  - Load into `users_table`

- **Transformation 3**:  
  - SQL JOIN on `userid`  
  - Group & summarize total sales  
  - Output aggregated table `aggrsales`

### 📤 **Load**
All final outputs were loaded into a NeonDB PostgreSQL cloud database.

---

## 🚀 Job Orchestration

The ETL flow was orchestrated using a Pentaho Job file which includes:

- ✅ Start step  
- 🧾 SQL script to truncate old records  
- 🛠️ Sequential execution of 3 transformations  
- 📦 Final load to PostgreSQL

---

## 🧪 Results

- ✅ Data successfully cleaned and migrated
- ✅ Aggregated sales report created per user
- ✅ No job errors in end-to-end execution

---

---

## 📁 Project Structure

```bash
PentahoPizzaPipeline/
├── etl_jobs/
│   ├── main_job.kjb
│   ├── sales_transform.ktr
│   ├── user_transform.ktr
│   └── join_aggr_transform.ktr
├── input_data/
│   └── User_pizza_sales.csv
├── output_data/
│   └── aggrsales_output.csv
├── screenshots/
│   └── *.png
├── README.md
├── .gitignore
└── LICENSE
```

![Screenshot 2025-07-01 160257](https://github.com/user-attachments/assets/7c1312b2-0cfe-43c8-9c61-f83a3e48ddb0)

![Screenshot 2025-07-01 180127](https://github.com/user-attachments/assets/b744a7f8-d972-4107-b478-22a435bbf2e6)
![Screenshot 2025-07-01 180134](https://github.com/user-attachments/assets/5571dfb8-3eb0-465e-bac0-01f8e5524fc8)

![Screenshot 2025-07-01 160211](https://github.com/user-attachments/assets/38203601-22a2-4eba-bb74-1895684cdc34)
