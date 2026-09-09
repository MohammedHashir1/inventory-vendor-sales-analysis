# inventory-vendor-sales-analysis
End-to-end inventory and vendor sales analysis using Python, SQL, SQLite and Power BI.
# Inventory & Vendor Sales Analysis

An end-to-end data analytics project analyzing **vendor performance, inventory turnover, purchasing behavior, profitability, and unsold inventory capital** using Python, SQL, SQLite, and Power BI.

The project processes a large inventory dataset, performs SQL-based data aggregation, applies statistical and business analysis using Python, and presents key findings through an interactive Power BI dashboard.

---

## 📌 Project Overview

The objective of this project is to transform raw inventory, purchasing, sales, and vendor data into actionable business insights.

The analysis focuses on:

* Vendor and brand sales performance
* Gross profit and profit margins
* Inventory turnover
* Purchase contribution by vendor
* Bulk purchasing and unit purchase prices
* Unsold inventory and capital locked in stock
* Low-performing and high-performing vendors
* Statistical comparison of vendor profitability

---

## 🛠️ Tools & Technologies

| Tool                 | Purpose                                      |
| -------------------- | -------------------------------------------- |
| **Python**           | Data analysis and feature engineering        |
| **Pandas**           | Data manipulation and KPI calculations       |
| **NumPy**            | Numerical analysis                           |
| **SQL**              | Data extraction and aggregation              |
| **SQLite**           | Database storage and querying                |
| **SQLAlchemy**       | Database connectivity                        |
| **SciPy**            | Statistical testing and confidence intervals |
| **Matplotlib**       | Data visualization                           |
| **Seaborn**          | Exploratory data visualization               |
| **Power BI**         | Interactive dashboard and business reporting |
| **Jupyter Notebook** | Analysis environment                         |

---

## 📊 Dataset

The project uses multiple raw CSV files containing inventory, purchasing, sales, vendor invoice, and pricing information.

### Dataset Scale

* **6 raw CSV files**
* Approximately **15.8 million rows**
* Data consolidated into a SQLite database
* Final vendor-level analysis performed using a consolidated `vendor_sales_summary` table

> **Note:** The raw CSV files are not included in this repository due to their large size.

---

## 🔄 Data Pipeline

The project follows an end-to-end analytics workflow:

```text
Raw CSV Files
      ↓
Python / Pandas
      ↓
Data Ingestion
      ↓
SQLite Database
      ↓
SQL Queries & Table Joins
      ↓
Vendor Sales Summary
      ↓
Python Feature Engineering
      ↓
KPI & Statistical Analysis
      ↓
Power BI Dashboard
      ↓
Business Insights
```

The ingestion process uses Python and database connectivity to load the raw datasets into SQLite.

The analytical layer uses SQL to combine relevant purchasing, sales, vendor invoice, and pricing information before further analysis in Pandas.

---

## 🧮 Key KPIs

The analysis calculates several business KPIs to evaluate vendor and inventory performance.

### Gross Profit

```text
Gross Profit = Total Sales - Total Purchase Cost
```

Measures the profit generated from sales after accounting for purchase costs.

### Profit Margin

```text
Profit Margin = Gross Profit / Total Sales × 100
```

Measures profitability relative to sales.

### Stock Turnover

Used to identify vendors and products with slow-moving or excess inventory.

### Sales-Purchase Ratio

Compares sales activity against purchasing activity to evaluate inventory movement.

### Unsold Inventory Value

```text
Unsold Inventory Value =
(Total Purchase Quantity - Total Sales Quantity)
× Purchase Price
```

Measures the amount of capital currently tied up in unsold inventory.

---

## 📈 Power BI Dashboard

The Power BI dashboard provides an interactive view of overall sales, profitability, vendor performance, brand performance, and inventory.

### Key Dashboard Metrics

* **Total Sales:** ~$441M
* **Gross Profit:** ~$134M
* **Profit Margin:** **38.72%**
* **Unsold Inventory Capital:** ~$2.71M

The dashboard includes:

* KPI cards
* Vendor-level sales analysis
* Brand-level sales analysis
* Profitability analysis
* Inventory analysis
* Vendor contribution analysis
* Scatter plots
* Bar charts
* Donut/pie charts

The dashboard enables users to explore performance across different vendors and brands.

---

## 💡 Key Business Insights

### 🏆 Top Vendor Performance

**Diageo North America** emerged as the leading vendor, generating approximately **$68M in sales**.

This highlights the vendor's significant contribution to overall sales performance.

### 📦 Inventory Risk

Vendors with **Stock Turnover below 1** were analyzed to identify potential slow-moving inventory and excess stock.

These vendors may require inventory optimization or purchasing adjustments.

### 💰 Capital Locked in Inventory

The analysis identified approximately **$2.71M in unsold inventory capital**.

Reducing slow-moving and dead stock could help release working capital and improve inventory efficiency.

### 📉 Low-Sales / High-Margin Brands

Brands with relatively low sales but high profit margins were identified as potential candidates for:

* Promotional campaigns
* Pricing adjustments
* Increased sales focus
* Distribution optimization

### 🛒 Bulk Purchasing Analysis

Purchase quantities were divided into small, medium, and large order groups to investigate whether larger purchasing volumes were associated with lower unit purchase prices.

### 📊 Statistical Analysis

A **95% confidence interval analysis** and **two-sample t-test** were performed to compare profit margins between top-performing and low-performing vendors.

This helped evaluate whether the observed differences in profitability were statistically significant.

---

## 📂 Project Structure

```text
inventory-vendor-sales-analysis/
│
├── README.md
│
├── inventory_vendor_sales_analysis.ipynb
│
├── data/
│   └── README.md
│
├── sql/
│   └── vendor_analysis.sql
│
├── powerbi/
│   └── inventory_vendor_dashboard.pbix
│
├── database/
│   └── README.md
│
└── requirements.txt
```

> Large raw datasets and database files can be excluded from the repository to keep the project lightweight.

---

## ▶️ How to Run the Notebook

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/inventory-vendor-sales-analysis.git
```

### 2. Navigate to the project

```bash
cd inventory-vendor-sales-analysis
```

### 3. Install the required Python packages

```bash
pip install pandas numpy matplotlib seaborn scipy sqlalchemy
```

Or, if `requirements.txt` is provided:

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
inventory_vendor_sales_analysis.ipynb
```

### 5. Database Requirement

The notebook expects the SQLite database:

```text
myinventory.db
```

and the relevant table:

```text
vendor_sales_summary
```

If the database is not included in the repository, recreate it using the project's data ingestion pipeline before running the analysis.

---

## 📌 Project Outcomes

This project demonstrates practical experience in:

* Large-scale data ingestion
* Python data analysis
* SQL querying and table joins
* SQLite database management
* Feature engineering
* Business KPI development
* Exploratory data analysis
* Statistical analysis
* Inventory analytics
* Vendor performance analysis
* Power BI dashboard development
* Translating data into business recommendations

---

## 👤 Author

**Your Name**

Aspiring Data Analyst | Python | SQL | Power BI | Data Analytics

---

⭐ If you found this project interesting, feel free to explore the notebook and dashboard.
