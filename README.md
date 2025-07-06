# Spotify end-to-end data engineering project

### Intorduction
The purpose of this project is to build an ETL pipeline by using the Spotify API on AWS. it will extract the data from Spotify API, transform it to a desired format, and load it it into an AWS data store.

### Architecture
![Architecture Diagram](https://github.com/mtmehmood/spotify-end-to-end-data-engineering-project/blob/main/Spotify%20ETL%20Diagram.jpg)

### About Dataset/API
This API contains information about the music, artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used

1.	**S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.

2.	**AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDB, or other AWS services.
3.	**Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to track metrics, collect and monitor log files, and set alarms.
4.	**Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data formats, and builds the metadata to create an AWS Glue Data Catalog.
5.	**Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can integrate the Glue Data Catalog with other AWS services, such as Athena.
6.	**Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.


### Install Packages

```
pip install pandas
pip install numpy
pip install spotify
```

### Project Execution Flow
Extract Data from API → Lambda Trigger → Run Extract Code → Store Raw Data → Trigger Transform Function → Transform Data and Load It → Query Using Athena
