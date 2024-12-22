# Stock Market Real-Time Data Analysis Using Kafka and AWS Service

This project demonstrates the real-time processing and analysis of simulated stock market data using Kafka, with data storage and analysis on AWS services like S3, AWS Glue, and AWS Athena.

## Project Overview

The goal of this project is to simulate real-time stock market data, stream it using Apache Kafka, store it in AWS S3, and process the data using AWS Glue and Athena for analysis. It showcases a scalable, event-driven architecture for real-time data pipelines.

### Tech Stack

- **Python**: Used for simulating stock market data and interacting with AWS services.
- **Apache Kafka**: For real-time streaming of stock market data.
- **AWS S3**: Storage of stock market data.
- **AWS Glue**: For transforming and preparing data for analysis.
- **AWS Athena**: For querying the data stored in AWS S3 using SQL.

## Project Components

### 1. **Simulating Stock Market Data**
   A Python script generates simulated stock market data, including stock symbols, prices, volume, and timestamps. This data is then pushed into Kafka topics for real-time streaming.

### 2. **Kafka Streaming**
   - Kafka Producers push the simulated stock data to Kafka topics in real time.
   - Kafka Consumers read data from these topics for further processing.

### 3. **Storing Data in AWS S3**
   - The real-time stock data is stored in Amazon S3 for persistent storage.
   - Data is organized by time intervals (e.g., hourly or daily) and saved as CSV or Parquet files for easy querying.

### 4. **AWS Glue ETL**
   - AWS Glue is used to create an ETL pipeline that transforms the raw stock data into a structured format.
   - The data is then cataloged for easier querying in Athena.

### 5. **AWS Athena Queries**
   - AWS Athena is used to query the stock data stored in S3 using SQL.
   - Analytics can be performed to gain insights into stock trends, averages, and price movements.

## Requirements

- **Python 3.x**: Make sure to have Python 3 installed.
- **Kafka**: Install and set up Apache Kafka.
- **AWS Account**: You need access to AWS S3, Glue, and Athena services.
- **AWS CLI**: AWS CLI tool for accessing AWS services from your terminal.
