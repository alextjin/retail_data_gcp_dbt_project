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

![image](https://github.com/user-attachments/assets/843e1427-3dc6-4606-9aa9-41dff73d7eab)


Getting Start
================

## Prerequisites
- Docker and Astro CLI needed to be installed
- Also, register an account for Soda & Google Cloud Services

## Project Content
### Dataset
This project is using the online retail data from Kaggle (https://www.kaggle.com/datasets/tunguz/online-retail)

### Pipeline
Your Astro project contains the following files and folders:

- dags: This folder contains the Python files for your Airflow DAGs. By default, this directory includes one example DAG:
    - `example_astronauts`: This DAG shows a simple ETL pipeline example that queries the list of astronauts currently in space from the Open Notify API and prints a statement for each astronaut. The DAG uses the TaskFlow API to define tasks in Python, and dynamic task mapping to dynamically print a statement for each astronaut. For more on how this DAG works, see our [Getting started tutorial](https://docs.astronomer.io/learn/get-started-with-airflow).
- Dockerfile: This file contains a versioned Astro Runtime Docker image that provides a differentiated Airflow experience. If you want to execute other commands or overrides at runtime, specify them here.
- include: This folder contains any additional files that you want to include as part of your project. It is empty by default.
- packages.txt: Install OS-level packages needed for your project by adding them to this file. It is empty by default.
- requirements.txt: Install Python packages needed for your project by adding them to this file. It is empty by default.
- plugins: Add custom or community plugins for your project to this file. It is empty by default.
- airflow_settings.yaml: Use this local-only file to specify Airflow Connections, Variables, and Pools instead of entering them in the Airflow UI as you develop DAGs in this project.

Deploy Your Project Locally
===========================

1. Start Airflow on your local machine by running 'astro dev start'.

This command will spin up 4 Docker containers on your machine, each for a different Airflow component:

- Postgres: Airflow's Metadata Database
- Webserver: The Airflow component responsible for rendering the Airflow UI
- Scheduler: The Airflow component responsible for monitoring and triggering tasks
- Triggerer: The Airflow component responsible for triggering deferred tasks

2. Verify that all 4 Docker containers were created by running 'docker ps'.

Note: Running 'astro dev start' will start your project with the Airflow Webserver exposed at port 8080 and Postgres exposed at port 5432. If you already have either of those ports allocated, you can either [stop your existing Docker containers or change the port](https://docs.astronomer.io/astro/test-and-troubleshoot-locally#ports-are-not-available).

3. Access the Airflow UI for your local Airflow project. To do so, go to http://localhost:8080/ and log in with 'admin' for both your Username and Password.

You should also be able to access your Postgres Database at 'localhost:5432/postgres'.

Deploy Your Project to Astronomer
=================================

If you have an Astronomer account, pushing code to a Deployment on Astronomer is simple. For deploying instructions, refer to Astronomer documentation: https://docs.astronomer.io/cloud/deploy-code/

Contact
=======

The Astronomer CLI is maintained with love by the Astronomer team. To report a bug or suggest a change, reach out to our support.
