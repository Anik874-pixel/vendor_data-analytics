# Vendor Data Processing Workflow

## Overview
This project implements an end-to-end data processing pipeline for large-scale vendor and inventory datasets.  
It focuses on ingesting raw CSV data into a relational database, transforming it using SQL and Pandas, and generating business performance metrics for analytical reporting and dashboard visualization.

The workflow simulates a real-world analytics engineering process involving data ingestion, cleaning, aggregation, and KPI generation.

---

## Dataset
- Multi-table vendor inventory dataset
- Includes purchases, sales, freight, and pricing information
- Large files handled using memory-efficient sampling (`nrows`) during ingestion for local processing

---

## Pipeline Steps

### 1️⃣ Data Ingestion
- CSV files loaded using Pandas  
- Stored into SQLite tables via SQLAlchemy  
- Modular ingestion scripts implemented  
- Logging enabled for traceability  

### 2️⃣ Data Aggregation
- SQL CTE-based queries join multiple tables
- Vendor-level summary table generated

### 3️⃣ Data Cleaning & Transformation
- Missing value handling
- Type conversions
- String normalization
- Feature engineering using Pandas

### 4️⃣ KPI Computation
- Gross Profit  
- Profit Margin  
- Stock Turnover  
- Sales-to-Purchase Ratio  

### 5️⃣ Exploratory Analysis
- Notebook-based EDA and inspection of transformed data

### 6️⃣ Dashboard Visualization
The processed dataset will be used to build an interactive dashboard (Power BI) to visualize vendor performance metrics and business insights.

---

## Tech Stack
- Python
- Pandas
- SQLite
- SQL (Joins, Aggregations, CTEs)
- Logging
- Git & GitHub
- Power BI (Dashboard — upcoming)

---

## How to Run

### Install dependencies
```bash
pip install pandas sqlalchemy

