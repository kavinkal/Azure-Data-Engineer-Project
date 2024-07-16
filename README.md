# Azure-Data-Engineer-Project
This project builds an End-to-End Azure Data Engineering Solution. A  services which is Azure Data Factory(Data Ingestion, ETL pipeline creation),Azure Databricks(Transformation) and finally loads the data into ADLS Gen2.

# Project Goal 
The goal is to create a ETL pipeline using ADF which can take an On-premise Database such as the Microsoft SQL Server Management System (SSMS) and move it to ADLS Gen2 container and apply transformation using ADB.

Data Ingestion to the Cloud to perform transformation and store the data in the structured form in ADLS to use for report and analysis purpose.
# Prerequisites:

1.Data Ingestion
2.ETL techniques using Azure Cloud Services
3.Data Transformation
4.Data Loading

# Part 1: Data Ingestion
1.Restore the AdventureWorksLT2017 Database from the .bak file.
![WhatsApp Image 2024-07-16 at 6 10 01 PM](https://github.com/user-attachments/assets/d5b20e78-86cf-4890-9969-0772b2253eee)
2.Setup the Microsoft Integration Runtime between Azure and the On-premise SQL Server.                  
3.Create a Copy Pipeline which loads the data from local on-premise server into Azure Data Lake Storage Gen2 "Bronze" directory.
Note that the Data store is stored in "Parquet format" in ADLS Gen2 storage folders.
![image](https://github.com/user-attachments/assets/c9ceaf81-3ba2-47de-952e-9e708644ebd8)

# Part 2: Data Transformation
Initially mounting the path from ADLS Gen2 to AZB
Data is Loaded into Azure Databricks where can create PySpark Notebooks. Cluster nodes, and compute automatically managed by the Databricks service. The Initial Data is cleaned and processed in two steps. Bronze to Silver and Silver to Gold.

1. In Bronze to Silver transformation, we apply Attribute Type Changes and move this preprocessed data from Bronze to Silver folders.
2. In Silver to Gold transformation, we rename the Attributes to follow similar Naming Convention throughout the database. Then we move this into Gold folder.
3. The Final Gold-level Data is suitable for business reporting and making dashboard visualizations. Gold-level data is in "Delta" format.
![image](https://github.com/user-attachments/assets/0c5d2dba-6fc2-4f05-b391-6ed06e3d98cf)
Launch Azure Databricks and run transformations using these notebooks "bronze to silver" and "silver to gold".
![image](https://github.com/user-attachments/assets/eae0bc30-aad9-4dcc-b6a3-d09f5d43b676)
Integrating the spark notebook to the ADF using Notebook activity.
![image](https://github.com/user-attachments/assets/82820f59-f975-43fa-9ad9-1f31d5647e25)
# Part:3 Data Loading
After doing the data cleaning the data is stored in the silver container in the delta format.Here, i simply overwrites the data. As like same post this activity done some aggregation and changes un the data then moved to gold container.








