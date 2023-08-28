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
1. Create EC2 instance and connect ssh to terminal via CLI. Download apache kafka and make sure java is installed.
2. Run kafka and zookeeper servers in separate terminal windows. Make sure to Run in public IP (edit settings).
3. Create topic and Start producer and consumer in separate sessions. Here, make sure to put the Public IP of EC2 Instance:9092.
4. Run Producer and Consumer python files to test connection and load data from CSV file to AWS.
5. Create a new folder in S3 bucket to load stteaming data into it.
6. In AWS Glue, create a crawler with appropriate IAM admin role and database. Run this crawler to update catalog.
7. In AWS Athena, this new table should be reflected and SQL queries can be excecuted.




Inspiration from Darshil Parmar
