### **Data Ingestion Overview**



This project uses Azure Data Factory (ADF) to ingest multiple Tokyo Olympics datasets from GitHub into the Raw Zone of Azure Data Lake Storage Gen2 (ADLS Gen2).A single ADF pipeline orchestrates the end-to-end ingestion, ensuring each table is copied reliably and in sequence.



**Pipeline Name: Copy\_Data\_Athletes**



The pipeline consists of a chain of Copy Data activities that load the following source datasets:



**1. Athletes**

**2. Coaches**

**3. Genders**

**4. Medals**

**5. Teams**



Each activity ingests a CSV dataset from GitHub and writes it into the corresponding raw folder in ADLS Gen2.



How the Pipeline Works: 



&nbsp;	1. Copy Athletes - First step in the ingestion flow



&nbsp;		**Copies athletes.csv → raw/athletes/**



&nbsp;	2. Copy Coaches - Begins after Athletes succeed



&nbsp;		**Copies coaches.csv → raw/coaches/**



&nbsp;	3. Copy Genders - Triggered after Coaches



&nbsp;		**Copies gender.csv → raw/genders/**



&nbsp;	4. Copy Medals -Triggered after Genders



&nbsp;		**Copies medals.csv → raw/medals/**



&nbsp;	5. Copy Teams - Final ingestion step



		**Copies teams.csv → raw/teams/**

