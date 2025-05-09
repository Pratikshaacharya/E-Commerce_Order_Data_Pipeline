# E-Commerce_Order_Data_Pipeline
This project focuses on designing and implementing a scalable, efficient, and automated data pipeline for an e-commerce dataset using Azure Data Factory, Databricks, Delta Lake, and Tableau. The goal is to ingest, transform, and visualize data while ensuring data governance and scalability.

## Architecture Overview

<img width="463" alt="image" src="https://github.com/user-attachments/assets/3768b118-c94a-4f0d-b32d-ff713c9271ae" />


## Tech Stack:<br>
<b>Azure Data Factory (ADF)</b>: Data ingestion from GitHub & ADLS<br><br>
<b>Databricks Autoloader</b>: Incremental data processing<br><br>
<b>Databricks</b>: Data transformations<br><br>
<b>Unity Catalog</b>: Schema governance, access control, and metadata management<br><br>
<b>Azure Data Lake Storage(Bronze → Silver → Gold)</b>: Centralized storage for raw, transformed, and processed data<br><br>
<b>Tableau</b>: Data visualization for business insights<br>

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
