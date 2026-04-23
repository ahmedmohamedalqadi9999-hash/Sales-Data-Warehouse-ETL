# 📊 Sales Data Warehouse & ETL Pipeline

## 📌 Project Overview
This project demonstrates a complete **Data Engineering end-to-end solution**. The goal was to build a robust Data Warehouse (DWH) for sales data using a **Star Schema** architecture. I developed an automated **ETL Pipeline** using **Python** to extract data from a transactional SQL Server database, perform necessary transformations, and load it into a structured Data Warehouse for analytical purposes.

## 🛠️ Technology Stack
* **Database:** Microsoft SQL Server (Source: OLTP, Destination: DWH)
* **Programming:** Python (Pandas, pyodbc, SQLAlchemy)
* **Development Environment:** Jupyter Notebook (`.ipynb`)
* **Modeling Tools:** Miro / Draw.io
* **Version Control:** Git & GitHub

## 🗄️ Data Warehouse Architecture (Star Schema)
The system is designed using a Star Schema to optimize query performance for BI and reporting.

### 🖼️ Schema Diagram
<img width="1920" height="1080" alt="Screenshot (199)" src="https://github.com/user-attachments/assets/f39d1402-6e85-4267-95ee-c9757620de55" />


### 🔹 Tables Structure:
* **Fact Table:** `fact_sales` (Contains metrics like Quantity, Unit Price, Total Price, and Foreign Keys).
* **Dimension Tables:**
    * `dim_product`: Product categories and sub-categories.
    * `dim_customer`: Customer profile data.
    * `dim_salesman`: Sales team details and locations.
    * `Dim_Date`: Calendar attributes for time-series analysis (Year, Quarter, Month, Weekend, etc.).

## ⚙️ ETL Pipeline Workflow
The pipeline handles the data lifecycle in three main stages:

### 🖼️ Pipeline Design
<img width="1920" height="1080" alt="Screenshot (198)" src="https://github.com/user-attachments/assets/323d7a60-83fc-4fd7-a288-432b84938d38" />


1.  **Extract:** Connecting to the source SQL Server and fetching raw sales data using `pyodbc`.
2.  **Transform:**
    * Data cleaning and handling missing values.
    * Joining tables (e.g., Products with Categories) using Pandas.
    * Mapping source data to the dimensional model.
3.  **Load:**
    * **Full Load:** Initial ingestion of historical data.
    * **Incremental Load:** Logic implemented to update the DWH with only new/modified records.

## 📂 Repository Structure
* `app2.ipynb`: The main Jupyter Notebook containing the ETL Python code.
* `SQLQuery1.sql` / `SQLQuery2.sql`: SQL scripts for creating the DWH tables (DDL).
* `images/`: Contains architecture and pipeline diagrams.

## 🚀 How to Run
1.  Execute the SQL scripts in your SQL Server instance to create the DWH schema.
2.  Update the connection string in `app2.ipynb` with your server credentials.
3.  Run the notebook cells to execute the ETL process.

---
**Developed by Ahmed Alqadi** *Data Engineer | 2026 Portfolio*
