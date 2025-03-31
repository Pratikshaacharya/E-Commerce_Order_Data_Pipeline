# E-Commerce_Order_Data_Pipeline
This project focuses on designing and implementing a scalable, efficient, and automated data pipeline for an e-commerce dataset using Azure Data Factory, Databricks, Delta Lake, and Tableau. The goal is to ingest, transform, and visualize data while ensuring data governance and scalability.

## Architecture Overview

<img width="463" alt="image" src="https://github.com/user-attachments/assets/3768b118-c94a-4f0d-b32d-ff713c9271ae" />


Tech Stack:\n
Azure Data Factory (ADF): Data ingestion from GitHub & ADLS\n
Databricks Autoloader: Incremental data processing\n
Databricks: Data transformations\n
Unity Catalog: Schema governance, access control, and metadata management\n
Delta Lake (Bronze → Silver → Gold): Structured and scalable data transformation\n
Tableau: Data visualization for business insights\n

## Data Flow

1. Data Ingestion:
ADF extracts raw data from GitHub and stores it in Azure Data Lake Storage (ADLS).
Databricks Autoloader loads incremental data into Bronze Layer (ADLS - Bronze Container).

2. Data Transformation (Bronze → Silver → Gold):
Bronze Layer: Stores the raw data.
Silver Layer: Cleans, formats, and applies business logic.
Gold Layer: Aggregates and enriches data for reporting.
Unity Catalog: Manages schema governance & access control.

3. Data Visualization:
Delta Tables registered under Unity Catalog.
Tableau dashboards provide insights on sales trends, customer behavior, and inventory.
