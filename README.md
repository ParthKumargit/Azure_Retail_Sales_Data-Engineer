🚀 End-to-End Azure Retail Data Engineering Pipeline
📌 Project Overview

This project implements an end-to-end retail data engineering pipeline on Microsoft Azure.

The solution integrates data from multiple sources, including Azure SQL Database and REST API, and processes the data through a Medallion Architecture (Bronze, Silver, Gold) using Azure Data Factory, Azure Data Lake Storage Gen2 and Azure Databricks.

The final Gold-layer dataset is designed for Power BI reporting and retail sales analysis.

🎯 Problem Statement

* The retail business maintains its data across multiple sources:

Transaction data in Azure SQL Database
Product data in Azure SQL Database
Store data in Azure SQL Database
Customer data available through a REST API in JSON format

* The business needs a centralized data platform that can:

Ingest data from multiple sources.
Store raw data in a centralized data lake.
Clean and standardize the data.
Remove duplicate records.
Combine transaction, customer, product and store information.
Calculate important sales metrics.
Create an analytics-ready dataset.
Provide the processed data for Power BI dashboards.



* Technical Requirements
Azure Data Factory for data ingestion and orchestration.
ADLS Gen2 for centralized data storage.
Azure Databricks for data transformation.
PySpark for data processing.
Delta Lake for Silver and Gold data.
Power BI for visualization.
Implement Bronze → Silver → Gold Medallion Architecture.


* Gold Layer

The Silver data is transformed into a business-oriented sales summary.

The data is grouped by:

Transaction Date
Product
Category
Store
Location

The following metrics are calculated:

Total Quantity Sold
sum("quantity")
Total Sales Amount
sum("total_amount")
Number of Transactions
countDistinct("transaction_id")
Average Transaction Value
avg("total_amount")

📈 Final Output

The final output is a business-ready retail sales dataset that can be consumed by Power BI.

The dataset enables analysis of:

Total sales
Quantity sold
Number of transactions
Average transaction value
Sales by product
Sales by category
Sales by store
Sales by location
Sales trends over time
