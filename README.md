# Stock-Market-Analysis

## About
It involves real-time data streaming & analysis of Stock Market data with over 100K records(Index,Date,Open,High,Low,Close,Adj Close,Volume,CloseUSD). Data is loaded the data into an S3 bucket incrementally with an interval of 1 second. Data Engineering project using technologies like: Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

## AWS Services used
<ul>
<li>S3</li>
<li>EC2 (Kafka and Zookeeper)</li>
<li>Glue (Crawler and Catalog)</li>
<li>Athena</li>
</ul>

## Architechture Diagram
![image](https://github.com/ragarasagna/Stock-Market-Analysis/assets/51982703/20d4f14a-e9df-4120-8301-e2bbd410f225)


## Steps
1. Create EC2 Instance and SSH Connection:
  *Launch an EC2 instance with your desired settings.
  *Use the CLI to connect to the instance via SSH.
  *Ensure that Java is installed on the instance.
2.Install and Run Apache Kafka:
  *Download and set up Apache Kafka on the EC2 instance.
 *Run Kafka and Zookeeper servers in separate terminal windows.
  *Configure Kafka to listen on a public IP (update settings as needed).
3.Topic Creation and Producer/Consumer Setup:
  *Create a Kafka topic using appropriate commands.
  *Start Kafka producer and consumer in separate terminal sessions.
  *Use the Public IP of the EC2 instance and port 9092 for Kafka connections.
4.Test Connection and Data Loading:
  *Run Python scripts for the producer and consumer to test the Kafka connection.
  *Verify that data can be loaded from a CSV file to Kafka and consumed properly.
5.Prepare S3 Bucket for Streaming Data:
  *Create a new folder within your chosen S3 bucket to hold the streaming data.
6.AWS Glue Crawler for Catalog Updating:
  *Set up an appropriate IAM admin role for AWS Glue.
  *Create an AWS Glue crawler to scan and catalog the data in your S3 bucket.
  *Run the Glue crawler to ensure your data's metadata is updated in the Glue Data Catalog.
7.AWS Athena for Querying:
  *Open AWS Athena and verify that the newly cataloged table is reflected.
  *Write and execute SQL queries to analyze the data directly from the Glue Data Catalog.






Inspiration from Darshil Parmar
