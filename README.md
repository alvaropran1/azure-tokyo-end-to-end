# Azure End-To-End Tokyo Olympics Data Engineering Project

## Overview
Modern data pipeline leveraging Azure services for end-to-end data processing and analytics.

## Pipeline Flow

<img width="1183" alt="Screenshot 2024-11-19 at 3 37 31 PM" src="https://github.com/user-attachments/assets/7b3d9e04-db14-4166-9779-e828883161d9">


### 1. Data Ingestion
- **Data Source** → Various input sources (databases, files, APIs)
- **Azure Data Factory** → Orchestrates data movement
- **Data Lake Gen 2** → Raw data storage

### 2. Processing
- **Azure Databricks** → Data transformation and processing
- **Data Lake Gen 2** → Transformed data storage

### 3. Analytics & Visualization  
- **Azure Synapse Analytics** → Enterprise analytics
- **Visualization Tools**
  - Power BI
  - Looker Studio
  - Tableau

For this project, we will be using Looker

## Key Benefits
- Automated pipeline
- Scalable architecture
- Real-time processing
- Enterprise security
- Cost optimization
- Advanced analytics

## Technologies
- Azure Data Factory
- Azure Data Lake Gen2
- Azure Databricks
- Azure Synapse Analytics
- Power BI/Looker/Tableau

## Steps taken

In this Azure Data Engineering project, I implemented an end-to-end data pipeline following industry best practices. Here's a summary of the steps I took:

### 1. Project Setup:
   - Created an Azure project and storage account
   - Set up a container with separate folders for raw and transformed data

### 2. Data Ingestion:
   - Used Azure Data Factory to extract data from CSV files hosted on GitHub
   - Configured the data source as HTTP and CSV format
   - Set up the sink to store data in the Azure Data Lake Gen2 raw-data folder
   - Validated and debugged the pipeline to ensure proper data ingestion

![Screenshot 2024-11-23 at 8 23 40 PM](https://github.com/user-attachments/assets/c99600c3-999e-4e0c-bc7c-3cf22b2f1322)

### 3. Data Storage:
   - Utilized Azure Data Lake Gen2 for storing both raw and transformed data
   - Implemented a folder structure to separate raw and processed data

![Screenshot 2024-11-23 at 8 24 24 PM](https://github.com/user-attachments/assets/88a06bcc-1db2-491e-a7b0-33d2bf16921d)


### 4. Data Transformation:
   - Created a Databricks workspace for data processing
   - Attempted to mount Azure Data Factory to access the data (Note: Faced access issues due to using a university Azure account)
   - Prepared Spark code to read data from the raw folder and transform it
   - Analyzed and validated the data to ensure it matched the original format
   - Repeated the process for multiple tables (medals, teams, coaches, etc.)

### 5. Data Validation:
   - Verified the transformed data in the Azure container
   - Downloaded and compared the processed data with the original format to ensure accuracy

Throughout the project, I focused on implementing best practices such as:
- Separating raw and transformed data
- Using Azure Active Directory and Key Vault for security (planned but not fully implemented due to access restrictions)
- Designing the pipeline for automatic processing of new data
- Implementing a bronze (raw), silver (partially processed), and gold (final) layer approach for data quality and governance

While I couldn't complete all steps due to access limitations, this project demonstrated my ability to design and partially implement a robust data engineering solution using Azure services.
