![Python](https://img.shields.io/badge/python-3.10-blue)
![Apache Spark](https://img.shields.io/badge/Spark-3.4-orange)
![Hadoop](https://img.shields.io/badge/Hadoop-3.4-red)


# Distributed Analysis of Yelp Data Using Hadoop and Spark

## Overview
This project implements a distributed ETL and analytics pipeline on the Yelp Open Dataset using Apache Spark and Hadoop. The objective was to analyze large-scale business and user behavior patterns in Arizona salons by processing multi-gigabyte JSON datasets across multiple entities .

The system performs distributed ingestion, transformation, aggregation, and analytical querying to extract scalable business and user-level insights.


## Problem Statement
Yelp generates high-volume, semi-structured data containing business metadata, user profiles, and reviews.
Processing this data on a single machine is inefficient and does not scale.
This project demonstrates how distributed systems can be used to process, transform, and analyze such data efficiently.

## Architecture Overview
The data processing workflow follows a distributed pipeline:
- Yelp JSON files are stored in HDFS
- Data is filtered and transformed using Spark SQL
- Columnar formats are used for optimized querying
- Aggregated results are analyzed using PySpark

## Tech Stack
- **Languages:** Python (PySpark), SQL
- **Distributed Systems:** Apache Hadoop (HDFS), Apache Spark
- **Processing Engine:** Spark SQL, DataFrames
- **Environment:** Ubuntu 22.04 LTS (Virtual Machine)
- **Tools:** Jupyter Notebook, VS Code, Git
- **Data Format:** JSON, Parquet

## Dataset
This project uses the Yelp Open Dataset, which includes business, user, and review data.
Only the structured Yelp dataset is used for analysis.

All datasets were processed in JSON format and handled using distributed Spark transformations.

Dataset download instructions are provided in `data/README.md`.

## Project Milestones

### Milestone 1: Business-Level Analysis
This phase focuses on analyzing Yelp businesses operating in Arizona.
The dataset is filtered geographically and transformed for efficient aggregation.
Spark SQL is used to analyze business ratings, review counts, categories, and attributes.

Notebook and Report is available for the same.

### Milestone 2: User-Level Analysis
This phase analyzes user behavior associated with the selected business category.
User activity, review contributions, and engagement patterns are examined using distributed aggregations.

Notebook and Report is available for the same. 

## Setup & Execution
This project is executed in a local distributed environment.
Detailed setup and verification steps for Hadoop, Spark, and PySpark are documented in:

`config/spark_hadoop_setup.md`

---

## Key Engineering Components

### 1. Distributed Data Ingestion
Loaded multi-gigabyte Yelp JSON datasets into Spark DataFrames using PySpark with schema inference and filtering logic for Arizona-based salons.

### 2. Data Transformation & Normalization
- Filtered businesses by state (AZ) and category ("Salon")
- Created structured temporary SQL views
- Normalized attributes for aggregation
- Joined USER, REVIEW, TIP, and BUSINESS datasets

### 3. Distributed Aggregations
Implemented Spark SQL queries to compute:
- User engagement metrics
- Elite user growth trends
- Review count distributions
- Sentiment-based aggregations
- Postal code performance metrics

### 4. Performance-Oriented Processing
- Leveraged distributed joins and partition-based aggregations
- Reduced computation overhead through SQL optimization
- Processed multi-million records efficiently across cluster execution

---

## Analytical Insights

### User-Level Insights
- 65.7% of users contributed 1–10 reviews
- Elite user growth steadily increased from 2011–2021
- Top contributors significantly influence engagement

### Business-Level Insights
- 30.5% of salons categorized under Beauty & Spas
- High-performing postal codes identified (85704, 85712)
- Strong correlation between engagement and ratings

---

## Key Takeaways / Skills Demonstrated

- Built distributed data pipelines using Apache Hadoop and Apache Spark
- Processed large semi-structured JSON datasets efficiently
- Transformed data into Parquet for optimized analytics
- Performed business-level and user-level analysis using Spark SQL
- Developed reproducible notebooks with clear documentation
- Applied data engineering best practices for scalable analytics

## Future Improvements

- Partitioned Parquet storage for improved read performance
- Incremental ETL support
- Airflow-based orchestration
- Dashboard integration for real-time monitoring

