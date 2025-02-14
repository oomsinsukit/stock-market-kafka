# Stock Market Real-Time Data Analysis Using Kafka and AWS Service

This project demonstrates the real-time processing and analysis of simulated stock market data using Kafka, with data storage and analysis on AWS services like S3, AWS Glue, and AWS Athena.

## Introduction 
In this project, you will execute an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka.

We are going to use different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

## Architecture 
<img src="Architecture.png">

### Tech Stack
- **Python**: Used for simulating stock market data and interacting with AWS services.
- **Apache Kafka**: For real-time streaming of stock market data.
- **AWS S3**: Storage of stock market data.
- **AWS Crawler**: For automatically discovering and cataloging the structure of the data in S3.
- **AWS Glue**: For transforming and preparing data for analysis.
- **AWS Athena**: For querying the data stored in AWS S3 using SQL.
- **AWS EC2**: For running Kafka brokers and other processing components.

## Project Components

### 1. **Simulating Stock Market Data**
   "A Python script simulates stock market data, including stock symbols, prices, volume, and timestamps, using data ingested in real-time from yfinance. This simulated data is then pushed into Kafka topics for real-time streaming."

### 2. **Kafka Streaming**
   - Kafka Producers push the simulated stock data to Kafka topics in real time.
   - Kafka Consumers read data from these topics for further processing.

### 3. **Storing Data in AWS S3**
   - The real-time stock data is stored in Amazon S3 for persistent storage.
   - Data is organized by time intervals (e.g., hourly or daily) and saved as CSV or Parquet files for easy querying.

### 4. **AWS Crawler**
   - AWS Glue Crawler is used to automatically discover the structure and schema of the data stored in S3.
   - The crawler creates metadata tables in the AWS Glue Data Catalog, making it easier for Athena to query the data.
   - Once the data is cataloged by the Crawler, it will be ready for transformation using AWS Glue.

### 5. **AWS Glue ETL**
   - AWS Glue is used to create an ETL pipeline that transforms the raw stock data into a structured format.
   - The data is then cataloged for easier querying in Athena.

### 6. **AWS Athena Queries**
   - AWS Athena is used to query the stock data stored in S3 using SQL.
   - Analytics can be performed to gain insights into stock trends, averages, and price movements.

### 7. **AWS EC2**
   - **Kafka on EC2**: You can deploy Kafka brokers on an EC2 instance to handle the real-time streaming of stock market data. Kafka requires distributed brokers for scalability and fault tolerance, and EC2 instances provide the necessary infrastructure to host and manage these brokers.
   - **Running Scripts on EC2**: You can run the Python scripts (Kafka producers, consumers, and data simulation) on EC2 instances to process data and interact with AWS services.
   - Ensure that the EC2 instances have proper security groups and IAM roles to interact with S3, Glue, and other AWS services.

## Requirements

- **Python 3.x**: Make sure to have Python 3 installed.
- **Kafka**: Install and set up Apache Kafka.
- **AWS Account**: You need access to AWS S3, Glue, Athena, and Glue Crawlers.
- **AWS CLI**: AWS CLI tool for accessing AWS services from your terminal.

## Acknowledgements

This project was inspired by the tutorial from [DarshilParmar](https://www.youtube.com/embed/KerNf0NANMo) on YouTube. The concepts and code were adapted from their tutorial.
