# Cloud-based Data Ingestion from S3 to Snowflake with Apache Airflow

## Overview

This project is hosted entirely in the cloud on an EC2 instance running Apache Airflow. Its primary objective is to efficiently ingest data from S3 to Snowflake while providing notifications upon successful job completion.

## Workflow
<img src="images/Flowchart.png" alt="Flowchart" width="500"/>

## Steps
1. **Data Storage in S3:**
   - Data is stored in S3, ready for ingestion.

2. **EC2 Instance Setup:**
   - An EC2 instance is created, and Apache Airflow is installed within a Python environment on the same instance.

3. **Warehouse Structure Creation:**
   - Execute the Snowflake Warehouse DDL script ([Snowflake Warehouse DDL.txt](link_to_file)) to establish the required structure. This includes creating a Staging table connected to S3 and the Target table, *city_info*.

4. **ETL Job with PySpark:**
   - **ETL Job Name:** [airflow_snowflake_s3_email.py](link_to_code)
     - 4.1. Use S3 key sensor to detect any file uploaded to S3 every 3 seconds.
     - 4.2. Move the data from the staging table to the target table.
     - 4.3. Send an email notification after successful data ingestion.

## Output

Link to Output Picture: [Output Picture](link_to_output_picture)

## Hosted Machine

EC2 instance

## Language Used

![PySpark Logo](link_to_pyspark_logo)

Feel free to explore the provided links to delve deeper into specific components of the project!
