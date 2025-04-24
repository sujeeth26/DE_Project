# End-to-End Azure Data Pipeline for API Ingestion & Analysis

## Overview

This project demonstrates the design and implementation of an end-to-end data pipeline on Azure. The pipeline ingests data from REST APIs, processes and transforms the data, and stores it in a structured format for reporting and analysis.

The project follows the **Medallion Architecture** with three layers:
- **Bronze Layer:** Raw data ingested into Azure Data Lake.
- **Silver Layer:** Cleaned and transformed data using PySpark in Azure Databricks.
- **Gold Layer:** Curated and optimized data stored in Delta format for analytics.

## Components

1. **Data Ingestion**  
   Data is ingested from REST APIs into Azure Data Lake (Bronze Layer) using **Azure Data Factory** (ADF).
   
2. **Data Transformation**  
   Data is cleaned and transformed using **PySpark** in **Azure Databricks** (Silver Layer).

3. **Data Storage**  
   The processed data is stored in **Delta format** (Gold Layer) to optimize query performance and data consistency.

4. **Incremental Data Processing**  
   The pipeline supports incremental data updates with parameterized pipelines and looped ingestion logic.

## Architecture

- **Bronze Layer (Raw Data):** Raw data is ingested from REST APIs into **Azure Data Lake**.
- **Silver Layer (Cleaned Data):** The raw data is cleaned and transformed using **PySpark** in **Azure Databricks**.
- **Gold Layer (Curated Data):** Final processed and curated data is stored in **Delta Lake** for fast and efficient querying.

## Tools & Technologies Used

- **Azure Data Factory (ADF)**: For orchestrating the data pipeline.
- **Azure Data Lake**: For storing raw and processed data.
- **Azure Databricks**: For transforming data using **PySpark**.
- **PySpark**: For data cleaning, transformation, and processing.
- **Delta Lake**: For optimized data storage and querying.
- **Medallion Architecture**: To structure the data pipeline into layers (Bronze, Silver, Gold).

## Getting Started

### Prerequisites

- Azure account with access to **Azure Data Factory**, **Azure Data Lake**, and **Azure Databricks**.
- Basic knowledge of **Azure services** and **data engineering** concepts.

### Steps to Run the Project

1. **Ingest Data:**  
   Use **Azure Data Factory** to set up REST API ingestion into **Azure Data Lake** (Bronze layer).

2. **Transform Data:**  
   Create a **Databricks notebook** using **PySpark** to clean and transform the raw data (Silver layer).

3. **Store Data:**  
   Store the cleaned and processed data in **Delta format** in the **Gold layer** in **Azure Data Lake**.

4. **Reporting and Analysis:**  
   Use **Azure SQL** or any BI tool to query and generate reports from the final curated data.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
