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
<ul><li>Launch an EC2 instance with your desired settings.</li>
  <li>Use the CLI to connect to the instance via SSH.</li>
  <li>Ensure that Java is installed on the instance.</li></ul>
2.Install and Run Apache Kafka:
  <ul><li>Download and set up Apache Kafka on the EC2 instance.</li>
 <li>Run Kafka and Zookeeper servers in separate terminal windows.</li>
  <li>Configure Kafka to listen on a public IP (update settings as needed).</li></ul>
3.Topic Creation and Producer/Consumer Setup:
  <ul><li>Create a Kafka topic using appropriate commands.</li>
  <li>Start Kafka producer and consumer in separate terminal sessions.</li>
  <li>Use the Public IP of the EC2 instance and port 9092 for Kafka connections.</li></ul>
4.Test Connection and Data Loading:
  <ul><li>Run Python scripts for the producer and consumer to test the Kafka connection.</li>
  <li>Verify that data can be loaded from a CSV file to Kafka and consumed properly.</li></ul>
5.Prepare S3 Bucket for Streaming Data:
  <ul><li>Create a new folder within your chosen S3 bucket to hold the streaming data.</li></ul>
6.AWS Glue Crawler for Catalog Updating:
  <ul><li>Set up an appropriate IAM admin role for AWS Glue.</li>
  <li>Create an AWS Glue crawler to scan and catalog the data in your S3 bucket.</li>
  <li>Run the Glue crawler to ensure your data's metadata is updated in the Glue Data Catalog.</li></ul>
7.AWS Athena for Querying:
  <ul><li>Open AWS Athena and verify that the newly cataloged table is reflected.</li>
  <li>Write and execute SQL queries to analyze the data directly from the Glue Data Catalog.</li></ul>






Inspiration from Darshil Parmar
