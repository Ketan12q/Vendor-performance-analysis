# 🧾 Vendor Performance Analysis – Retail Inventory & Sales

An end-to-end analytics project evaluating vendor efficiency, sales performance, and inventory dynamics to guide strategic purchasing and profitability decisions.  
The workflow integrates SQL for ETL, Python for analytics, and Power BI for visualization**.

---

## 📌 Table of Contents
- [Overview](#overview)  
- [Business Problem](#business-problem)  
- [Dataset](#dataset)  
- [Tools & Technologies](#tools--technologies)  
- [Project Structure](#project-structure)  
- [Data Cleaning & Preparation](#data-cleaning--preparation)  
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
- [Research Questions & Insights](#research-questions--insights)  
- [Dashboard](#dashboard)  
- [How to Run This Project](#how-to-run-this-project)  
- [Final Recommendations](#final-recommendations)  
- [Author & Contact](#author--contact)  

---

## 🔎 Overview
This project analyzes **vendor contribution, profitability, and inventory turnover** to uncover insights for **pricing strategies, procurement planning, and sales optimization**.  
It demonstrates a **full analytics pipeline**:  
- SQL → Data ingestion and transformation  
- Python → Cleaning, analysis, and hypothesis testing  
- Power BI → Interactive dashboards and reporting  

---

## 💼 Business Problem
Retail organizations face challenges in balancing **inventory costs, vendor reliability, and profitability**. This project addresses:  
- Identifying underperforming vendors & products  
- Vendor contribution to total revenue & margins  
- Evaluating cost efficiency of bulk orders  
- Detecting inventory bottlenecks and slow-moving stock  
- Validating profitability differences across vendors  

---

## 📂 Dataset
- Multiple **CSV files** located in the `/data/` folder (sales, inventory, vendor details).  
- Summary tables generated during SQL ingestion are used for reporting and analysis.  

---

## 🛠 Tools & Technologies
- **SQL** → ETL, filtering, joins, aggregations  
- **Python** → Pandas, NumPy, Matplotlib, Seaborn, SciPy  
- **Power BI** → Visual dashboards & performance KPIs  
- **Excel** → Supporting reports  

---

## 📁 Project Structure
vendor-performance-analysis/
│── README.md
│── requirements.txt
│── .gitignore
│
├── notebooks/ # Jupyter notebooks
│ ├── exploratory_data_analysis.ipynb
│ └── vendor_performance_analysis.ipynb
│
├── scripts/ # Python scripts
│ ├── ingestion_db.py
│ └── get_vendor_summary.py
│
├── dashboard/ # Power BI dashboards
│ └── vendor_performance_dashboard.pbix
│
├── reports/ # Additional reports
│ └── vendor_sales_summary.xlsx
│
└── data/ # Datasets
├── raw/ (original files - ignored on GitHub)
└── sample/ (small demo datasets)

yaml
Copy code

---

## 🧹 Data Cleaning & Preparation
- Removed invalid transactions (e.g., Gross Profit ≤ 0, Sales Quantity = 0).  
- Standardized vendor/product identifiers.  
- Converted datatypes & merged lookup tables.  
- Built **vendor-level summary tables** for analysis.  

---

## 📊 Exploratory Data Analysis (EDA)
- **Negative values:** Loss-making sales & below-cost margins detected.  
- **Outliers:** High freight charges (up to 250K), extreme unit costs.  
- **Correlations:**  
  - Sales Qty ↔ Purchase Qty (0.999 → nearly perfect)  
  - Profit Margin ↔ Sales Price (-0.18 → negative correlation)  

---

## ❓ Research Questions & Insights
- **Which vendors to promote?** → 190+ brands with high margins but low sales.  
- **Top vendors:** 10 suppliers account for ~65% of purchases → over-reliance risk.  
- **Bulk purchasing:** Large orders reduce unit cost by ~70%.  
- **Inventory turnover:** $2.7M unsold stock highlights inefficiencies.  
- **Profitability differences:** Hypothesis testing confirms vendor margin strategies vary significantly.  

---

## 📈 Dashboard
The Power BI dashboard includes:  
- Vendor-wise sales, margins, and performance heatmaps  
- Inventory turnover metrics  
- Bulk purchasing impact  
- Profitability & risk indicators  

📌 *Preview:*  
![Dashboard Screenshot](assets/dashboard_screenshot.png)  

---

## ⚙️ How to Run This Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/vendor-performance-analysis.git
   cd vendor-performance-analysis
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Ingest raw data into SQL:

bash
Copy code
python scripts/ingestion_db.py
Generate vendor summary tables:

bash
Copy code
python scripts/get_vendor_summary.py
Run notebooks for analysis:

bash
Copy code
notebooks/exploratory_data_analysis.ipynb
notebooks/vendor_performance_analysis.ipynb
Open Power BI dashboard:

text
Copy code
dashboard/vendor_performance_dashboard.pbix
✅ Final Recommendations
Diversify vendor partnerships to mitigate dependency risks.

Reprice and promote slow-moving high-margin products.

Adopt optimized bulk purchase strategies.

Reduce unsold inventory with clearance campaigns.

Focus marketing on low-performing vendors with potential.

**👨‍💻 Author & Contact**
Ketan Mangla
B.Tech CSE | Data Analytics 

📧 Email: ketanmangla989@gmail.com
🔗 LinkedIn: linkedin.com/in/ketan-mangla98