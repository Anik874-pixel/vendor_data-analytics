
---

## 🔄 Pipeline Workflow

### 1️⃣ Data Ingestion
- Reads CSV files from `/data`
- Loads them into Pandas
- Writes tables to SQLite database
- Logging enabled for traceability

### 2️⃣ Vendor Summary Creation
- SQL joins across multiple tables
- Aggregated metrics per vendor
- Includes:
  - Purchases
  - Sales
  - Freight
  - Pricing

### 3️⃣ Data Cleaning & Feature Engineering
New analytics features generated:
- Gross Profit
- Profit Margin
- Stock Turnover
- Sales to Purchase Ratio

---

## ▶️ How to Run

### Install dependencies
```bash
pip install pandas sqlalchemy
