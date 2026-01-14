![Python](https://img.shields.io/badge/python-3.10-blue)
![Apache Spark](https://img.shields.io/badge/Spark-3.4-orange)
![Hadoop](https://img.shields.io/badge/Hadoop-3.4-red)


# Distributed Analysis of Yelp Data Using Hadoop and Spark

## Overview
This project performs large-scale analysis of Yelp business and user review data for the state of Arizona. 
The dataset consists of semi-structured JSON files that require distributed processing for efficient analysis.
Apache Hadoop and Apache Spark are used to build scalable data pipelines and perform analytical workloads.

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
Due to size and licensing constraints, the raw data is not included in this repository.

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

## Results Summary
The analysis demonstrates how distributed data processing frameworks can efficiently support large-scale analytics.
Insights at both the business and user levels highlight the value of scalable data pipelines for analytical workloads.

## Key Takeaways / Skills Demonstrated

- Built distributed data pipelines using Apache Hadoop and Apache Spark
- Processed large semi-structured JSON datasets efficiently
- Transformed data into Parquet for optimized analytics
- Performed business-level and user-level analysis using Spark SQL
- Developed reproducible notebooks with clear documentation
- Applied data engineering best practices for scalable analytics

