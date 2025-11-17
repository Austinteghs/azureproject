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

| Layer  | Purpose                        | Storage Tech               | Data Format      |
|--------|--------------------------------|---------------------------|----------------|
| Bronze | Raw, immutable source data      | ADLS Gen2                 | JSON/Parquet   |
| Silver | Cleaned, validated, enriched    | ADLS Gen2                 | Delta Lake     |
| Gold   | Business-level aggregates       | Azure SQL Database        | SQL Tables     |

**Core Services:**  
- Azure Data Lake Storage Gen2: Bronze & Silver layers  
- Azure Databricks with Delta Live Tables: Transformations  
- Azure Data Factory: Pipeline orchestration  
- Azure SQL Database: Gold layer analytics  

## 🛠️ Technical Implementation
**Pipeline Details:**  
- **Data Ingestion:** Automated Spotify API collection; stored as JSON in Bronze layer  
- **Transformation:** Silver layer: schema validation, cleansing, deduplication; Gold layer: aggregations and analytics  
- **Data Quality:** Automated validation, expectation-based checks, lineage tracking, error alerting  

