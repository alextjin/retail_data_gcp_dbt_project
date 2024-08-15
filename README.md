Project Overview
========

This repository contains a personal project designed to enhance my skills in Data Engineering. It focuses on developing data pipelines with Airflow, BigQuery, dbt, Soda and more.

> [!IMPORTANT]
> Many architectural choices and decisions in this project may not make the most efficent sense on purpose for the sake of practicing and learning.

Solution Architecture
================

### Tools & Services

| Category                    | Tool                                                                                                                           | Description                                                                                           |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Static Site Generator       | ![Astro](https://img.shields.io/badge/Astro-FF5A1F?style=flat-square&logo=astro&logoColor=white)                               | Astro is used to build fast, content-focused static websites.                                         |
| Containerization Platform   | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)                            | Docker is used to containerize applications, ensuring consistent environments across development and production. |
| Cloud Platform              | ![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)           | Google Cloud Platform (GCP) provides cloud services and infrastructure for hosting and scaling applications. |
| Data Transformation Tool    | ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)                                     | dbt (data build tool) is used for transforming data inside the warehouse.                             |
| Workflow Orchestration      | ![Airflow](https://img.shields.io/badge/Airflow-2.6.1-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)             | Apache Airflow is used to programmatically author, schedule, and monitor workflows.                   |
| Data Quality Monitoring     | ![Soda](https://img.shields.io/badge/Soda-53B3CB?style=flat-square&logo=Soda&logoColor=white)                                  | Soda is used for data quality monitoring and alerting.                                                |
| Databases                   | ![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat-square&logo=google-bigquery&logoColor=white)               | BigQuery is a fully-managed, serverless data warehouse that enables scalable analysis over petabytes of data. |
| BI Visualization Tool       | ![Metabase](https://img.shields.io/badge/Metabase-509EE3?style=flat-square&logo=metabase&logoColor=white)                     | Metabase is used for business intelligence and data visualization.                                    |

### Pipeline
![image](https://github.com/user-attachments/assets/48fff9c7-3c5d-4e1b-91d7-72909f6e12ab)
1. The pipeline will first upload the Online_Retail.csv file to Google Cloud Storage
2. Then we will ingest the CSV file to BigQuery
3. Data Quality precheck before transformation
4. Conduct Data Transformation and break the raw data into a fact table and 3 dimension tables
5. Data Quality postcheck after transformation
6. Generate business report based on the invoices
7. Data Qaulity check on the reports
8. Visualise the business performance with metabase

Result Outcome
================
We will finally get 9 tables in BigQuery. 'report_year_invoices', 'report_product_invoices' & 'report_customer_invoices' are the business report tables and will be used for analytic reports.
![image](https://github.com/user-attachments/assets/e2fe4a1a-c865-4088-8eeb-e02cbb0f1ab0)

![image](https://github.com/user-attachments/assets/6b173c1a-c4b3-48b0-a7cb-8e37986b75cc)


