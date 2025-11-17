# Spotify Data Engineering Project on Azure

## 📋 Project Overview
A data engineering solution that processes Spotify listening data through a modern cloud architecture. Demonstrates end-to-end pipeline development from raw data ingestion to analytics-ready datasets using Azure services.

## 🎯 Business Objectives
- Build a scalable data platform for music listening analytics  
- Implement reliable data pipelines with quality checks  
- Enable historical analysis and real-time insights  
- Provide clean, structured data for BI and machine learning  

## 🏗️ Architecture
Here's a visual representation of the Spotify Data Engineering project:

![Spotify Data Engineering Project Diagram](https://github.com/Austinteghs/azureproject/blob/main/spotify%20data%20engineering%20project%20diagram.jpg)


**Data Layers (Medallion Architecture):**

| Layer  | Purpose                        | Storage Tech       | Data Format      |
|--------|--------------------------------|------------------|----------------|
| Bronze | Raw, immutable source data      | ADLS Gen2         | JSON/Parquet   |
| Silver | Cleaned, validated, enriched    | Delta Lake        | Delta Tables   |
| Gold   | Business-level aggregates       | Delta Lake  | Fact & Dimension Tables |

**Core Services:**  
- Azure Data Lake Storage Gen2: Bronze layer storage  
- Azure Databricks with Delta Live Tables: Transformation & pipeline orchestration  
- Azure Data Factory: Pipeline scheduling and ingestion  
- Databricks SQL Warehouse: Gold layer analytics  

## 🛠️ Technical Implementation
**Pipeline Details:**  
- **Data Ingestion:** Automated Spotify API + other sources; stored raw in Bronze layer  
- **Transformation:** Silver layer: schema validation, cleansing, deduplication; Gold layer: star schema & analytics-ready tables  
- **Data Quality:** Automated validation, expectation-based checks, lineage tracking, error alerting  
