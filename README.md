# Financial Transactions Fraud Analysis  
**Python Exploratory Data Analysis with Azure Data Engineering Architecture**

---

## Project Overview

This project focuses on the exploratory analysis of a financial transactions dataset containing **users**, **cards**, and **transaction records**. The primary objective is to understand customer behavior, card usage patterns, and transaction characteristics in the context of **financial fraud detection**.

While the original implementation included an end-to-end Azure Data Engineering pipeline, the scope of this repository centers on **Python-based data analysis**, with the Azure work retained as a separate architectural and engineering implementation of the same dataset.

---

## Dataset Description
[Transactions Fraud Dataset](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets).
The dataset consists of three core tables:

### 1. Users Dataset
Contains demographic and profile information for customers, including:
- Age and retirement age
- Employment and income attributes
- User identifiers linked to cards and transactions

### 2. Cards Dataset
Contains card-level information such as:
- Card type and ownership
- Card-to-user relationships
- Card lifecycle attributes

### 3. Transactions Dataset
Contains detailed transaction records including:
- Transaction amounts and timestamps
- Merchant and category details
- Transaction-level indicators relevant to fraud analysis

---

## Python-Based Analysis (Primary Focus)

The analysis is implemented entirely in **Python** using a Jupyter Notebook (`.ipynb`) and includes the following steps:

### Data Cleaning and Preprocessing
- Handling missing and inconsistent values
- Correcting data types (dates, numeric fields, categorical variables)
- Removing duplicates and invalid records
- Preparing clean, analysis-ready datasets

### Univariate Analysis
- Distribution analysis of transaction amounts
- User age and retirement age distributions
- Card usage frequency analysis
- Identification of outliers and anomalies

### Bivariate Analysis
- Relationships between transaction amount and fraud indicators
- User demographics vs transaction behavior
- Card attributes vs transaction patterns
- Behavioral trends that may indicate fraudulent activity

These analyses establish baseline behavioral patterns, highlight risk indicators, and prepare the data for potential downstream fraud modeling.

---

## Azure Data Engineering Work (Architectural Implementation)

In parallel to the Python analysis, the dataset was also implemented in an end-to-end Azure Data Engineering pipeline to demonstrate cloud-scale ingestion, transformation, and analytics.

### Azure Architecture Summary

- Multiple Azure Resource Groups created for:
  - Development
  - Test
  - SIT
  - UAT (Pre-production)
  - Production

- Two Azure Data Lake Storage (ADLS) accounts per environment:
  - Source storage
  - Destination storage

- Azure Databricks deployed per environment

---

### Data Ingestion and Transformation (Azure)

1. Dataset downloaded from Kaggle
2. Raw CSV files uploaded to ADLS bulk containers
3. Azure Data Factory (ADF) used to:
   - Ingest CSV data from source storage
   - Convert data from CSV to Parquet format
   - Store transformed data in destination storage
4. Azure Databricks used for:
   - Further transformations and validation
   - Optimised storage for analytics
5. Data consumed in Power BI for reporting and visualisation

> Parquet format was used to improve query performance and enable efficient columnar reads.

---

## Why Python Analysis Is the Focus of This Repository

- The Jupyter Notebook captures detailed analytical reasoning and insights
- Python EDA demonstrates **data understanding**, fraud intuition, and statistical exploration
- Azure implementation represents engineering scalability, while Python represents analytical depth

Together, both approaches show:
- End-to-end data engineering capability (Azure)
- Strong analytical and fraud-focused data analysis skills (Python)

---

## Technologies Used

### Python Stack
- Python
- Pandas
- NumPy
- Matplotlib / SciPy
- Jupyter Notebook

### Azure Stack (Architectural Work)
- Azure Data Factory
- Azure Data Lake Storage (ADLS Gen2)
- Azure Databricks
- Power BI

---

## Project Roadmap
<img width="1153" height="657" alt="Screenshot 2025-12-30 171017" src="https://github.com/user-attachments/assets/f1b2e1f6-8f0e-47fc-9efa-058635f0bd22" />


1. **Data Ingestion**  
   - Built pipelines using **Azure Data Factory (ADF)** to ingest raw banking transactions data from the source dataset into **Azure Data Lake Storage (ADLS)**.  
   - Ensured **idempotency and fault-tolerance** in data ingestion.

2. **Data Transformation & Processing**  
   - Leveraged **Databricks notebooks** for cleaning, transforming, and aggregating the raw data.  
   - Applied **PySpark** for distributed processing of large datasets.  
   - Generated analytical features relevant for fraud detection.

3. **Data Storage & Access**  
   - Stored transformed and curated datasets in **Azure Data Lake** for analytics and downstream applications.  
   - Configured partitioning strategies for **efficient retrieval and query performance**.

4. **Orchestration & Monitoring**  
   - Orchestrated the workflow using **ADF pipelines** with dependency-based triggers.  
   - Implemented **logging, monitoring, and error handling** to ensure pipeline reliability.

5. **Analytics & Insights**  
   - Enabled exploratory data analysis using Databricks notebooks.  
   - Created dashboards for visualising transaction patterns and potential fraud hotspots.

---
## Key Data Engineering Patterns Demonstrated

- **End-to-End ETL/ELT:** Full pipeline from ingestion to transformation and storage.  
- **Cloud-Native Data Engineering:** Leveraging ADF, ADLS, and Databricks for scalable cloud workflows.  
- **Data Partitioning & Optimization:** Efficient storage and query performance strategies.  
- **Fault-Tolerant Pipelines:** Idempotent ingestion, error handling, and retry mechanisms.  
- **Exploratory Analytics:** Enabling downstream analytics through structured, curated datasets.

---

## How to Run / Reproduce

1. Clone this repository.
2. Configure your Azure environment and ensure the following are set:
   - Azure Storage Account
   - Azure Data Factory instance
   - Databricks workspace with access to ADLS
3. Upload the dataset to your ADLS raw container.
4. Run the ADF pipelines to orchestrate ingestion and processing.
5. Access transformed data from the curated container in ADLS for analysis.

---

## References

- [Azure Data Factory Documentation](https://docs.microsoft.com/en-us/azure/data-factory/)  
- [Azure Databricks Documentation](https://docs.microsoft.com/en-us/azure/databricks/)  
- [Kaggle Transactions Fraud Dataset](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets)  
- [Vision Board Inspiration](https://www.youtube.com/watch?v=coVFXnVnBAc)

