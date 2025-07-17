# 🎯 End-to-End Data Engineering Project

---

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
