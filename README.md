
[![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=flat&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)
[![Airflow](https://img.shields.io/badge/Apache%20Airflow-%23017CEE.svg?style=flat&logo=apache-airflow&logoColor=white)](https://airflow.apache.org/)
[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=flat&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Databricks](https://img.shields.io/badge/Databricks-%23FF3621.svg?style=flat&logo=databricks&logoColor=white)](https://databricks.com/)
[![PySpark](https://img.shields.io/badge/PySpark-%23E35A16.svg?style=flat&logo=apachespark&logoColor=white)](https://spark.apache.org/)
[![DBT](https://img.shields.io/badge/dbt-%23FF694B.svg?style=flat&logo=dbt&logoColor=white)](https://www.getdbt.com/)
[![Django](https://img.shields.io/badge/Django-%23092E20.svg?style=flat&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-%23FF4B4B.svg?style=flat&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Whisper](https://img.shields.io/badge/Whisper%20(OpenAI)-%2346A29F.svg?style=flat&logo=openai&logoColor=white)](https://github.com/openai/whisper)
[![LangChain](https://img.shields.io/badge/LangChain-%23000000.svg?style=flat&logo=langchain&logoColor=white)](https://www.langchain.com/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-%23FFD21F.svg?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![SageMaker](https://img.shields.io/badge/SageMaker-%23232F3E.svg?style=flat&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/sagemaker/)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-%232671E5.svg?style=flat&logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![Python](https://img.shields.io/badge/Python-%233776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org/)



# 🎯 End-to-End Data Engineering Project



## 🚀 Introduction & Objectives

This project showcases my hands-on journey into the world of **Data Engineering**.

This project leverages the **YouTube API** and **Whisper transcriptions** to extract insights and enable analytics. Transcribed data is also used to fine-tune a **Large Language Model (LLM)**, allowing interaction with video content through **Langchain**.

### 🎯 Project Goals

- Build a complete **ELT data pipeline** using a modern data stack.
- Incorporate **DevOps, IaC, Docker, orchestration**, and cloud infrastructure.
- Provide **data mart insights** for video analytics.
- Fine-tune an **LLM** using course video transcripts.
- Support education by generating responses and synthetic datasets.
- Demonstrate full-stack **data engineering capabilities**.

---

## 📁 Project Structure

- `handlers-airflow`: Airflow orchestration with Terraform, Ansible, Docker Compose.
- `databricks`: Spark + Spark SQL transformation scripts.
- `application`: Django application with ECS deployment (Terraform + Docker).
- `app_dbt`: Data transformations and modeling using dbt Cloud.
- `aws`: AWS components (Glue, Lambda, Gateway, S3 triggers, Kinesis).
- `samples`: Output samples from various pipeline stages.
- `data`: Video data across raw → staging → intermediate → data mart.

---



---

## 📊 The Dataset

### 🧾 Data Sources

- **Transcripts (Parquet)**: Generated using Whisper AI for LLM training and analysis.
- **YouTube Metadata (JSON)**: Contains video IDs, titles, views, likes, comments, etc.

### 📌 Why This Dataset?

- **Custom-built** dataset to allow end-to-end modeling.
- Offers **nested JSON structures** and file format variety.
- Mimics a **real business scenario** for practical application.

### 🎯 Dataset Goals

- Normalize data (1NF, 2NF, 3NF) and use a **Snowflake schema**.
- Build **CTEs** and aggregate layers for the data mart.
- Use transformed data for both **analytics** and **LLM fine-tuning**.

---

## 🛠️ Technologies Used

### 💡 Stack Summary

This project was designed to simulate a **modern data engineering stack**, combining orchestration, infrastructure, cloud, and ML components.

### 🔧 Tools & Services

- **Infrastructure & CI/CD**:  
  `Terraform`, `Ansible`, `Docker`, `Docker Compose`, `GitHub Actions`

- **Orchestration**:  
  `Apache Airflow` (DAGs in Docker Compose)

- **Cloud (AWS)**:  
  `Glue`, `Kinesis`, `Lambda`, `S3`, `ECS`, `API Gateway`, `Athena`, `SageMaker`

- **Data Engineering**:  
  `Databricks`, `PySpark`, `Spark SQL`, `dbt`

- **ML/LLM**:  
  `Whisper (OpenAI)`, `Langchain`, `Hugging Face`, `LLM fine-tuning`

- **Application Layer**:  
  `Python`, `Django`, `Streamlit`, `REST API`

- **Architecture & Patterns**:  
  `Medallion Architecture`, `Factory Pattern`, `Abstract Classes`, `Pytest`

---

## 🔄 Pipeline Overview

- **Airflow DAGs**: Automate YouTube API extraction and preprocessing using Pandas and Spark.
- **Storage**: Metadata and transcripts are saved in **Amazon S3**.
- **Triggers**: S3 triggers launch **AWS Glue** and **Databricks** jobs.
- **Transformation**:
  - Flatten JSON
  - Remove duplicates
  - Enforce schema & test functions
- **Modeling**: dbt transforms intermediate data to **data mart** (Snowflake schema).
- **LLM Training**: Transcripts used to fine-tune LLM for answering video-related queries.

---
