# Real-Time Social Media Sentiment Analysis Pipeline

A scalable data engineering pipeline for processing social media data in real time, performing sentiment analysis, and generating actionable insights through Bronze, Silver, and Gold layers.

## 🚀 Project Overview

This project implements a **real-time social media sentiment analysis pipeline** using modern data engineering technologies.

The pipeline ingests JSON-based social media data, processes and cleans the data, performs sentiment analysis, applies data-quality checks, and produces aggregated metrics for dashboards and brand monitoring.

## 🔄 Project Flow

Source Data  
→ ADF / Data Ingestion  
→ ADLS Gen2  
→ Bronze Layer  
→ Silver Layer  
→ Gold Layer  
→ Data Quality & Testing  
→ Dashboards

**Airflow** is used to orchestrate the ETL workflow, while **Slack** provides failure notifications and monitoring.

## 🏗️ Architecture

- **Source:** Social media JSON data
- **Storage:** ADLS Gen2
- **Processing:** Azure Databricks / PySpark
- **Bronze:** Raw data
- **Silver:** Cleansed and validated data
- **Gold:** Aggregated sentiment metrics
- **Transformation:** dbt / Databricks
- **Testing:** Pytest
- **Orchestration:** Apache Airflow
- **Monitoring:** Slack
- **Version Control:** Git/GitHub

## 🥉 Bronze Layer

Stores raw social media events with minimal transformation.

**Example table:**
`social_catalog.raw.tweet_data`

## 🥈 Silver Layer

Cleans and transforms raw data by:

- Removing invalid records
- Handling missing values
- Parsing JSON
- Applying transformation rules
- Computing sentiment information

**Example table:**
`social_catalog.processed.valid_tweets`

## 🥇 Gold Layer

Creates business-level metrics for analysis and dashboards.

**Example table:**
`social_catalog.analytics.sentiment_stats`

Metrics can include:

- Positive/negative/neutral sentiment
- Sentiment scores
- Hourly sentiment trends
- Sentiment category distribution

## 🧪 Data Quality & Testing

**Pytest** is used to validate:

- Data completeness
- Data correctness
- Transformation logic
- Invalid records
- Sentiment-processing logic

## 🔄 Airflow Orchestration

Airflow coordinates the pipeline execution:

**Databricks Silver → dbt Gold → Pytest → Slack**

Airflow manages task dependencies, scheduling, retries, and failure handling.

## 🔔 Alerts & Monitoring

Slack notifications are triggered when pipeline tasks fail or when important anomalies are detected.

## 🎯 Objective

To build a scalable real-time data pipeline that transforms social media data into reliable sentiment insights for **brand monitoring and decision-making**.

## 🛠️ Technologies

`Azure` `ADLS Gen2` `Databricks` `PySpark` `Delta Lake` `dbt` `Apache Airflow` `Pytest` `Slack` `Python` `GitHub`
