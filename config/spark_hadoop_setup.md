# Spark and Hadoop Setup (Local VM)

This document describes the setup and verification steps for running the project in a local distributed environment.

## Environment
- Ubuntu 22.04 LTS (pre-configured virtual machine)
- Java Development Kit (JDK) installed for Hadoop and Spark
- Apache Hadoop for distributed storage and processing
- Apache Spark for distributed data processing
- PySpark (Python API for Spark)
- Jupyter Notebook / VS Code for interactive development (optional)

## Hadoop Commands
### Format Hadoop Filesystem (first-time setup only)
```bash
hdfs namenode -format

Start Hadoop Services
start-dfs.sh
start-yarn.sh

Verify Hadoop Installation

HDFS NameNode Web UI: http://localhost:9870

YARN ResourceManager Web UI: http://localhost:8088

Apache Spark
Verify Installation
spark-shell

PySpark
Start PySpark Shell
pyspark

Jupyter Notebook Integration

To use PySpark interactively in Jupyter Notebook:

pyspark


