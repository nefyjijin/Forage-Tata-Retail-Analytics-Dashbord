# Forage-Tata-Retail-Analytics-Dashbord
# 📊 Tata Retail Analytics Dashboard (Forage Virtual Experience)

## 📌 Project Overview
This project was completed as part of the **Tata Data Visualisation: Empowering Business with Effective Insights** virtual job simulation on Forage. The objective was to analyze an online retail dataset and create an interactive **Power BI** dashboard to help executive leadership understand sales performance, customer behavior, and global demand trends.



![Tata Retail Analytics Dashboard](path/to/your/dashboard-screenshot.png)

---

## 🎯 Key Performance Indicators (KPIs)
* **Total Revenue:** $10.64M
* **Total Demand (Quantity Sold):** 6M units
* **Total Customers:** 4K
* **Total Orders Placed:** 21K

---

## 🧹 Data Cleaning & Transformation (Power Query)
Before building the visuals, the raw dataset was cleaned and transformed in Power Query to ensure data accuracy and integrity:

1. **Removed Invalid Quantities:** Filtered out all records where `Quantity < 1` to eliminate canceled orders and return transactions.
2. **Removed Invalid Prices:** Filtered out rows where `UnitPrice < 0` (or `<= 0`) to remove bad debt adjustments and free/corrupted entries.
3. **Handled Missing Values:** Identified and managed missing values in `CustomerID` and `Description` fields to prevent skewed customer-level aggregations.
4. **Feature Engineering (Added Revenue Column):** Created a custom calculated column for `Revenue` using the formula:
   ```powerquery
   Revenue = [Quantity] * [UnitPrice]
   ```
5. **Standardized Data Types:** Updated and verified column data types across the dataset:
   * `InvoiceDate`: Date/Time (formatted for time-series analysis)
   * `Quantity`: Whole Number
   * `UnitPrice` & `Revenue`: Fixed Decimal Number (Currency)
   * `CustomerID`, `Country`, `StockCode`, `Description`: Text

---

## 📈 Dashboard Insights & Visuals
* **Monthly Revenue Trend:** Tracks revenue fluctuations across the calendar year, highlighting a strong seasonal surge starting in September and peaking in **November ($1.51M)** before dropping in December.
* **Top 10 Customers by Revenue:** Identifies high-value buyers driving repeat business, led by Customer ID `14646` ($0.28M) and Customer ID `18102` ($0.26M).
* **Top 10 Countries by Revenue and Quantity Sold (Excl. UK):** Compares international market performance outside the primary UK market, showing **Netherlands ($0.29M)**, **Ireland ($0.28M)**, and **Germany ($0.23M)** as top contributors.
* **Countries with Highest Demand:** A treemap and summary table breaking down unit demand by international region (e.g., Netherlands at 201K units, Ireland at 147K units, and Germany at 119K units).

---

## 🛠️ Tools & Technologies Used
* **Power BI Desktop:** Data modeling, DAX measures, and interactive dashboard design.
* **Power Query:** ETL (Extract, Transform, Load) and data cleaning.
* **DAX (Data Analysis Expressions):** Used to create dynamic measures for Total Customers, Total Orders, Total Revenue, and Total Demand.

---
