# Olist E-Commerce Data Engineering Project

## Overview
End-to-end data engineering pipeline built using 
PySpark on Databricks to analyze Brazilian 
E-Commerce data from Olist (Kaggle).

## Dataset
- Source: Kaggle - Brazilian E-Commerce by Olist
- Size: 100K+ orders
- Files: 9 CSV datasets

## Tech Stack
- PySpark
- Databricks (Serverless)
- Python

## Project Modules

### Module 1 - Data Ingestion & Exploration
- Loaded 9 CSV files into Spark DataFrames
- Explored schemas, null values, distributions
- Delivery time analysis
- Top selling products analysis

### Module 2 - Data Cleaning & Transformation
- Handled null values using drop/fill/impute strategies
- Removed duplicates
- Removed price outliers using percentile method
- Standardized payment type names
- Created product size categories (Small/Medium/Large)

### Module 3 - Data Integration & Aggregation
- Joined all 9 datasets into single master DataFrame
- Used broadcast join optimization
- Customer segmentation (High/Medium/Low Value)
- Seller performance metrics
- Product popularity metrics
- Weekday vs Weekend order analysis
- Hour of day distribution

### Module 4 - Spark Optimization
- Spark configuration tuning
- Broadcast join strategy
- Sort merge join strategy
- Bucket join strategy
- Window functions and rankings
- Advanced aggregations

### Module 5 - Data Serving Layer
- Saved processed data as Parquet format
- Saved as Delta Table for SQL querying
- Saved as CSV for business users

## Key Insights
- 99,441 customers and orders processed
- São Paulo has highest customer concentration
- Credit card is most popular payment method (76K+ orders)
- 96% of orders successfully delivered
- Average delivery time analyzed across all states

## How to Run
1. Download dataset from Kaggle:
   https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
2. Upload CSV files to Databricks Volume
3. Run notebooks in order:
   - Module 1 → Module 2 → Module 3 → Module 4 → Module 5
