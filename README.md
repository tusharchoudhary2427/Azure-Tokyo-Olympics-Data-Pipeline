# Azure-Tokyo-Olympics-Data-Pipeline

An end-to-end Azure Data Engineering pipeline built to process and analyze Tokyo Olympics 2021 datasets. The project uses Azure Data Factory to ingest raw CSV files from GitHub into Azure Data Lake Storage Gen2, and Azure Databricks (PySpark) to clean, transform, and generate structured results. The transformed data is saved back into ADLS Gen2 for easy analysis and reporting.

Key Features

  1. Ingests multiple raw CSV files from GitHub into ADLS Gen2 using Azure Data Factory
  2. Stores data in a clear Raw to Transformed folder structure
  3. Cleans, transforms, and joins datasets using PySpark in Azure Databricks
  4. Performs additional transformations such as counting athletes by sport
  5. Saves all processed results into the transformed container
  6. Simple and easy-to-understand design suitable for learning and showcasing ETL skills

Technologies Used

  1. GitHub – Source location for raw CSV files
  2. Azure Data Factory – Used for data ingestion from GitHub into ADLS Gen2
  3. Azure Data Lake Storage Gen2 – Used to store raw and transformed data
  4. Azure Databricks (PySpark) – Used for cleaning, transforming, and analyzing datasets
  5. PySpark – Used for writing transformation and aggregation logic

     
