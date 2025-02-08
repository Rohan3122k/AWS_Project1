# AWS_Project: California_Wildfire_Damage

# Storing and Querying Wildfire Data in AWS S3, Glue, and Athena : 
This project demonstrates how to efficiently store, catalog, and query wildfire damage data using AWS cloud services. The dataset, California_Wildfire_Damage.csv, contains historical wildfire incidents with details such as area burned, homes and businesses destroyed, financial loss, and causes. By leveraging AWS S3, Glue, and Athena, we created a serverless data pipeline for querying wildfire trends using SQL.

# Steps Implemented

1. Storing the Dataset in Amazon S3
- Created an S3 Bucket: wildfire-dataset-bucket (Region: us-east-2 - Ohio).
- Uploaded California_Wildfire_Damage.csv (7.6 KB, CSV format) to the S3 bucket.
- Applied best practices:
- Server-side encryption (SSE-S3) for data security.
- Bucket versioning enabled for data recovery.
- Block public access to prevent unauthorized access.

2. Creating an AWS Glue Data Catalog Table
- Created an AWS Glue Crawler (wildfire_crawler) to automatically infer the dataset schema.
- Defined a Glue Database (wildfire_db) to store metadata.
- Executed the crawler, which:
- Scanned the CSV file in S3.
- Generated a structured schema in the AWS Glue Catalog.
- Created a table: california_wildfire_damage.

3. Querying the Data Using Amazon Athena
- Connected Athena to the wildfire_db Glue database.
- Ran SQL queries to analyze the wildfire dataset:

