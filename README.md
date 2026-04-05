# 📊 TechHealth Analytics Data Warehouse

## 📌 Project Overview

This project implements a **Data Warehouse (OLAP system)** for a health-tech platform, designed to support analytical queries and business intelligence use cases.

It transforms transactional data from an OLTP system into a structured **star schema**, enabling efficient reporting on user behavior, health metrics, sales performance, and service operations.

---

## 🧱 Architecture

The warehouse is designed using a **star schema model**, with centralized fact tables connected to descriptive dimension tables.

### 🔹 Fact Tables

* **FactSales** → Stores transactional sales data
* **FactHealthMetrics** → Stores user activity, sleep, and stress metrics
* **FactServiceTickets** → Stores customer support interactions
* **FactDevices** → Stores device usage data

### 🔹 Dimension Tables

* **DimCustomer** → Customer demographics and subscription details
* **DimProduct** → Product information
* **DimDevice** → Device attributes
* **DimDate** → Time-based dimension for analysis

---

## ⚙️ ETL Process

The project includes ETL pipelines implemented using SQL:

* **Extract** → Data sourced from OLTP database (TechHealthDb)
* **Transform** → Data cleaned, joined, and converted into analytical format
* **Load** → Data inserted into fact and dimension tables

Key transformations:

* Conversion of dates into **DateKey (YYYYMMDD format)**
* Mapping of business keys to **surrogate keys**
* Joining multiple OLTP tables to create fact records

---

## 📊 Analytical Capabilities

The warehouse supports a variety of business insights, including:

* 📈 Revenue trends over time
* 🧑‍💻 Customer spending behavior
* 🏃 User activity vs engagement analysis
* 📱 Device usage patterns
* 🎫 Service ticket distribution and trends

Example analytical queries include:

* Top customers by spending
* Revenue by product category
* Monthly ticket trends
* Activity vs spending correlation

---

## 🗂️ Project Structure

```id="dw_struct_final"
TechHealth-DataWarehouse/
│
├── schema/       -- Fact and Dimension table definitions
├── etl/          -- Data loading and transformation scripts
├── analysis/     -- Business and analytical queries
├── diagrams/     -- Star schema diagram
│   └── star_schema.png
│
├── README.md
└── LICENSE
```

---

## ▶️ How to Run

1. Execute all scripts in the `schema/` folder
2. Run ETL scripts in the `etl/` folder
3. Execute queries in the `analysis/` folder

---

## 🛠️ Tech Stack

* **Database:** Microsoft SQL Server
* **Language:** T-SQL
* **Concepts:**

  * Star Schema Design
  * ETL (Extract, Transform, Load)
  * Data Modeling
  * Analytical Querying

---

## 🚀 Key Learnings

Through this project, I developed:

* Strong understanding of **data warehouse architecture (OLAP systems)**
* Hands-on experience with **star schema design**
* Ability to build **ETL pipelines from OLTP to OLAP systems**
* Skills in writing **analytical queries for business insights**
* Knowledge of **surrogate keys and dimensional modeling**

---

## 💡 Future Improvements

* Integration with Power BI for interactive dashboards
* Query performance optimization using indexing
* Expansion of dimensions for richer analytics
* Real-time or incremental ETL pipelines

---

## 📬 About

This project was built as part of my journey in learning data engineering and analytics. It represents a complete pipeline from structured data modeling to business-focused insights.

If you're a recruiter or reviewer, feel free to explore the repository and reach out for feedback or collaboration!
