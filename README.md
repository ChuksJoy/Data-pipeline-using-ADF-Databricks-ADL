# End-to-End Fraud Transactions Data Engineering Project

## Project Overview

In this project, I designed and implemented an end-to-end data engineering pipeline from scratch using Azure Data Factory, Azure Data Lake, and Databricks.  

The goal of this project was to create a robust, scalable, and production-ready pipeline for ingesting, transforming, and analysing a banking transactions dataset to detect potential fraud patterns. I leveraged the dataset from Kaggle: [Transactions Fraud Dataset](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets).

This project was inspired by Vision Board and the desire to demonstrate a complete modern cloud data engineering workflow.

---

## Project Roadmap
<img width="1655" height="880" alt="Screenshot 2025-12-30 170352" src="https://github.com/user-attachments/assets/31790af6-c46e-4233-a601-15c74192ba46" />


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

## Tech Stack

- **Cloud Platform:** Azure  
- **Data Orchestration:** Azure Data Factory  
- **Data Storage:** Azure Data Lake Storage (ADLS)  
- **Data Processing:** Databricks, PySpark  
- **Dataset:** Kaggle - [Transactions Fraud Dataset](https://www.kaggle.com/datasets/computingvictor/transactions-fraud-datasets)  
- **Monitoring & Logging:** ADF monitoring & Databricks logs  

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

