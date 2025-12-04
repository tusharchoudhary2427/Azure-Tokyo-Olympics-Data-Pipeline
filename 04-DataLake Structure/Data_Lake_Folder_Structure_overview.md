### **Azure Data Lake Folder Structure Overview:**



Azure Data Lake Storage Gen2 (ADLS Gen2) to organize the Tokyo Olympics 2021 datasets into two clear zones: Raw and Transformed. This structure helps maintain clean separation between ingested data and processed outputs, making the entire pipeline easy to understand and manage.



**Raw Zone (Input Data) ->** The Raw container stores all files exactly as they are ingested from GitHub using Azure Data Factory.

No cleaning or transformation is applied in this layer.



**Files stored:**



* athletes.csv
* coaches.csv
* genders.csv
* medals.csv
* teams.csv



**Transformed Zone (Processed Output) ->** The Transformed container stores the cleaned and processed results generated in Azure Databricks using PySpark. Each dataset is saved into its own folder, reflecting the structured output format.



**Folders created:**



* athletes
* coaches
* genders
* medals
* teams



Inside each folder, Databricks stores the processed results (CSV/Parquet) after applying transformations such as:



* Column cleanup
* Data validation
* Joins
* Aggregations (e.g., counting athletes per sport)



This zone contains data that is ready for analysis or loading into reporting tools.



