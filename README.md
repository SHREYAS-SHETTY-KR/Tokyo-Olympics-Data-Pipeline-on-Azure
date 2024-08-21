# Tokyo-Olympics-Data-Pipeline-on-Azure

This project demonstrates an end-to-end data engineering solution using Microsoft Azure services. The project focuses on building a data pipeline for Tokyo Olympic data, encompassing data ingestion, storage, transformation, and visualization. The pipeline is designed to integrate multiple Azure services, providing a seamless workflow from raw data to insightful dashboards.

![Screenshot 2024-08-21 192434](https://github.com/user-attachments/assets/bf776c6a-45a4-451c-82a2-3e8919c925d3)


## Technologies Used
- **Azure Data Factory**: For orchestrating and automating data ingestion.
- **Azure Data Lake Storage Gen2**: To store raw and transformed data.
- **Azure Databricks**: For data transformation and processing.
- **Azure Synapse Analytics**: For advanced analytics and data exploration.
- **Power BI**: For data visualization and creating interactive dashboards.

## Pipeline Overview
The data pipeline consists of several stages, each leveraging different Azure services:

1. **Data Source**: The initial data, including Athletes, Coaches, Medals, and Teams records, is gathered from various sources.
2. **Data Ingestion**: Azure Data Factory orchestrates the movement of raw data into the data lake.
3. **Raw Data Storage**: Data is stored in Azure Data Lake Storage Gen2 as raw files.
4. **Data Transformation**: Azure Databricks is used to clean, transform, and process the raw data.
5. **Transformed Data Storage**: The transformed data is stored back in Azure Data Lake Storage Gen2.
6. **Analytics**: Azure Synapse Analytics is used for advanced analytics and querying.
7. **Dashboarding**: The final insights are visualized using Power BI.

## Project Visuals

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/69f0c9b9-ca6a-4b76-b44d-c2dd9e9db1a9" alt="Image 1" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/fe11d052-5736-4dbb-98be-7d2320f0415b" alt="Image 2" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/e2f1090f-1a86-46cf-b4a9-b3404329c7b7" alt="Image 3" width="300"/></td>
  </tr>
</table>


## Project Execution Flow
1. **Ingest Data**: Use Azure Data Factory to pull data from the source and store it in the raw data zone of Azure Data Lake Storage.
2. **Transform Data**: Azure Databricks processes the raw data, transforming it into a structured format suitable for analysis.
3. **Store Transformed Data**: The processed data is saved in the transformed data zone within Azure Data Lake Storage.
4. **Analyze Data**: Use Azure Synapse Analytics to perform complex queries and data analysis.
5. **Visualize Data**: Create dashboards using Power BI to gain insights from the data.

## Project Structure

```
tokyo-olympic-data-pipeline/
├── 1_data_source/                             # Original data files (Athletes.csv, Coaches.csv, etc.)
│   ├── olympic_datasets/                      # Datasets for Tokyo Olympics
│   └── metadata/                              # Data source descriptions, data dictionaries
├── 2_data_ingestion/                          # Azure Data Factory configurations
│   ├── pipelines/                             # ADF pipeline definitions
│   └── linked_services/                       # Linked services and datasets
├── 3_raw_data_lake/                           # Storage for raw data in Azure Data Lake Gen2
│   ├── raw/                                   # Unprocessed data
│   └── archive/                               # Archived data versions
├── 4_data_transformation/                     # Data transformation with Azure Databricks
│   ├── notebooks/                             # Databricks notebooks for transformation
│   └── scripts/                               # Python/Scala scripts for processing
├── 5_transformed_data_lake/                   # Storage for processed data
│   ├── structured/                            # Organized and structured data
│   └── curated/                               # Data ready for analytics
├── 6_analytics_and_reporting/                 # Analytics using Azure Synapse and Visualization tools
│   ├── synapse_sql_pools/                     # SQL pools and queries in Synapse
│   ├── dashboards/                            # Power BI, Tableau, Looker Studio dashboards
│   └── reports/                               # Exported reports and visualizations
├── docs/                                      # Documentation
│   ├── architecture_diagrams/                 # Project architecture and flow diagrams
│   └── user_guide/                            # Instructions and project overview
├── .gitignore                                 # Git ignore file
├── README.md                                  # Project README file
└── requirements.txt                           # Python dependencies
```


## Conclusion
This project showcases the integration of various Azure services to build a robust and scalable data pipeline. By following this architecture, you can efficiently manage large datasets, perform complex data transformations, and gain valuable insights through advanced analytics and visualization tools.
