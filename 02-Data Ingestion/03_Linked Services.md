### **Linked Services:**



1. **Athletes\_Ingestion\_LS (HTTP)** **->** Used by ADF to fetch Athletes dataset from the GitHub raw file URL during ingestion.
   
2. **Coaches\_HTTP ->** Provides an HTTP connection for ADF to pull Coaches data directly from the source API/GitHub.
   
3. **Gender\_HTTP ->** Enables ADF to ingest Gender dataset via HTTP from the external GitHub link.
   
4. Medals\_HTTP **->** Used by ADF pipelines to retrieve Medals dataset through an HTTP-linked service.
   
5. **Teams\_HTTP ->** Facilitates ingestion of Teams dataset from GitHub using HTTP.
   
6. **tokyoolympicsadls (Azure Data Lake Gen2) ->** Stores all raw and transformed Olympic datasets; ADF writes raw files here and Databricks reads/writes transformed outputs.







