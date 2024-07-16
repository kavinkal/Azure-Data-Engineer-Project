# Azure-Data-Engineer-Project
This project builds an End-to-End Azure Data Engineering Solution. A  services which is Azure Data Factory(Data Ingestion, ETL pipeline creation),Azure Databricks(Transformation) and finally loads the data into ADLS Gen2.

#Project Goal 
The goal is to create a ETL pipeline using ADF which can take an On-premise Database such as the Microsoft SQL Server Management System (SSMS) and move it to ADLS Gen2 container and apply transformation using ADB.

Data Ingestion to the Cloud to perform transformation and store the data in the structured form in ADLS to use for report and analysis purpose.

1.Data Ingestion
2.ETL techniques using Azure Cloud Services
3.Data Transformation
4.Data Loading

#Prerequisites:
Part 1: Data Ingestion
1.Restore the AdventureWorksLT2017 Database from the .bak file.
![WhatsApp Image 2024-07-16 at 6 10 01 PM](https://github.com/user-attachments/assets/d5b20e78-86cf-4890-9969-0772b2253eee)
2.Setup the Microsoft Integration Runtime between Azure and the On-premise SQL Server.
3.Create a Copy Pipeline which loads the data from local on-premise server into Azure Data Lake Storage Gen2 "bronze" directory.
Note that the Data store is stored in "Parquet format" in ADLS Gen2 storage folders.
![image](https://github.com/user-attachments/assets/c9ceaf81-3ba2-47de-952e-9e708644ebd8)



