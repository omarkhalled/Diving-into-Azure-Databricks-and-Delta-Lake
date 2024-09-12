# Getting Into Azure Databricks and Delta Lake

## Overview
This repository contains notebooks that demonstrate the process of accessing Azure Data Lake using a service principal, transforming data, and working with Delta Lake to manage updates efficiently.

## Description
In this repository, I explore various tasks related to data engineering on Azure Databricks.

### Accessing Azure Data Lake using a service principal:
The notebook shows how to authenticate and securely access files stored in Azure Data Lake. This step demonstrates using service principals for access control.

### Loading and transforming CSV data:
I loaded a CSV file from Data Lake, specified its schema, and converted the file to Parquet format to take advantage of better storage efficiency and query performance.

### Creating a temporary view:
A temporary view was created from the Parquet file, allowing SQL-like querying within Databricks.

### Delta Lake conversion and updates:
Since updating Parquet files directly is not supported, I converted the Parquet table into a Delta table. This enabled me to perform updates and other ACID-compliant transactions on the data.

### Exploring the Delta transaction log:
I explored Delta Lake's transaction log to understand how it tracks changes to the data. This includes understanding the file structure, commit information, and the incremental nature of changes.

### Saving data in Delta format:
After the updates, the modified data was saved in Delta format to preserve version history and ensure better future performance with time-travel queries.

## Key Technologies

Azure Databricks, Azure Data Lake Storage, Delta Lake, Apache Spark (PySpark)
