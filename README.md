# 🚀 End-to-End Data Engineering Pipeline (AWS)

## 📌 Overview

This project demonstrates a complete data engineering pipeline that ingests raw JSON data, transforms it into structured format, and enables analytics using AWS services.

## 🏗️ Architecture

![Architecture](architecture/architecture.png)

## ⚙️ Tech Stack

* AWS S3 (Data Lake)
* AWS Lambda (Data Transformation)
* AWS Glue (Data Catalog & Crawling)
* AWS Athena (Query Engine)
* Apache Airflow (Orchestration)
* Python (Pandas, Boto3)

## 🔄 Pipeline Flow

1. Raw JSON data uploaded to S3 (`order_json_incoming`)
2. Lambda triggered automatically
3. JSON flattened and converted to Parquet
4. Processed data stored in S3 (`order_parquet_datalake`)
5. Glue crawler updates schema
6. Athena used for querying

## 📊 Sample Query

```sql
SELECT product_name, SUM(quantity) AS total_sold
FROM order_parquet_datalake
GROUP BY product_name;
```

## 📂 Project Structure

(Explain folders briefly)

## 🚀 How to Run

1. Upload JSON to S3
2. Lambda triggers automatically
3. Run Glue crawler
4. Query in Athena

## 📈 Key Learnings

* Handling nested JSON in ETL pipelines
* Serverless data processing using Lambda
* Building data lakes using S3
* Querying data using Athena

## 🧠 Future Improvements

* Add partitioning in S3
* Use Redshift instead of Athena
* Add dashboard (Tableau/Power BI)
