# Vendor Data Processing Workflow

## Overview
This project implements a lightweight end-to-end data processing workflow for large-scale vendor and inventory datasets.  
It simulates an analytics/data engineering pipeline involving ingestion of raw CSV data, relational storage, SQL aggregation, transformation using Python, and KPI computation for reporting.

The goal was to design a structured workflow resembling real-world analytics engineering processes while handling large datasets efficiently on local hardware.

---

## Motivation
This project was built to practice designing structured data workflows including:

- Data ingestion scripting  
- Logging and traceability  
- SQL-based relational aggregation  
- Python-driven transformations  
- Business KPI generation  

It reflects foundational skills relevant to data/analytics engineering roles.

---

## Dataset
- Multi-table vendor inventory dataset
- Includes purchases, sales, freight, and pricing information

**Original scale:** ~10M rows  

To enable efficient local execution, memory-aware sampling (`nrows`) was implemented during ingestion.

---

## Architecture / Data Flow

```
CSV Files
   ↓
Python Ingestion Script (ingestion_db.py)
   ↓
SQLite Database
   ↓
SQL Aggregation (get_vendor_summary.py)
   ↓
Python Processing (Vendor Data Analysis.py)
   ↓
Notebook Exploration
   ↓
Prepared Data for Dashboarding
```

---

## Pipeline Components

### Data Ingestion
`ingestion_db.py`
- Loads CSV files using Pandas
- Stores structured tables into SQLite
- Logging enabled for traceability
- Modular ingestion function design

### Aggregation
`get_vendor_summary.py`
- SQL queries with joins/CTEs
- Generates vendor-level summary tables

### Processing & Analysis
`Vendor Data Analysis.py`
- Cleaning and transformation
- Feature engineering
- KPI computation

### Exploratory Analysis
`notebooks/`
- Data inspection
- Validation of transformations
- Analytical exploration

---

## KPIs Computed
- Gross Profit  
- Profit Margin  
- Stock Turnover  
- Sales-to-Purchase Ratio  

---

## Tech Stack
- Python
- Pandas
- SQLite
- SQL (Joins, Aggregations, CTEs)
- Logging
- Jupyter Notebook
- Git & GitHub

---

## Repository Structure

```
notebooks/                 → EDA notebooks
Vendor Data Analysis.py    → Processing & KPI computation
get_vendor_summary.py      → SQL aggregation script
ingestion_db.py            → Data ingestion script
README.md
.gitignore
```

---

## How to Run

### Clone Repo
```bash
git clone https://github.com/Anik874-pixel/vendor_data-analytics
cd vendor_data-analytics
```

### Install Dependencies
```bash
pip install pandas sqlalchemy
```

### Run Pipeline
```bash
python ingestion_db.py
python get_vendor_summary.py
python "Vendor Data Analysis.py"
```

### Explore Notebook
Launch Jupyter:

```bash
jupyter notebook
```

Open files inside `notebooks/`

---

## Engineering Highlights
- Processed multi-million row dataset
- Implemented ingestion scripting with logging
- Integrated Python + SQL workflow
- Designed staged data processing flow
- Built business KPI computation layer

---

## Future Improvements
- Add requirements.txt
- Containerize with Docker
- Automate scheduling
- Cloud storage integration
- Distributed processing (Spark)

---

## Author
Aniket Kumar  
GitHub: https://github.com/Anik874-pixel
