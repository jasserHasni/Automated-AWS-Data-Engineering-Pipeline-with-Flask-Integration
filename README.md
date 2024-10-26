Project Overview:

This project involves designing and implementing a data engineering pipeline using AWS services. 
The pipeline is triggered by a Flask web application hosted on an EC2 instance. 
The Flask application includes a form that collects user inputs and initiates a series of data processing steps within AWS.


Objectives:
Utilize a Flask application to gather user input and trigger the data pipeline.
Host the Flask application on an AWS EC2 instance for reliable access and performance.
Implement a multi-step data engineering pipeline using AWS services to process the requests from the Flask application form.



Steps :

1-  Created an IAM user with acces to services (AWS S3,Amazon Athena,Cloudwatch,AWS lambda,Amazon DynamoDB Full Acces, AWS GLUE,AWS GLUE crawler)
2-  Hosted a flask application in an EC2 instance using nginx & Gunicorn  that contains a form to gather data from users 
3-  Created d dynamoDB database with 2 tables to save the data gathered from the users form
4-  Created an endpoint from dynamoDB stream 
5-  Triggered an aws Lambda function for each Update in the tables, that uses Spark to Transform the data and load it to an amazon S3 staging Bucket
6-  Created Layers of pandas and boto3 for the aws lambda handler because the apache scripts uses them
7-  Monitoring using Cloudwatch logs 
8-  Used AWS GLUE to transform and join the data,then saved it into an amazon s3 warehouse bucket
9-  Used AWS GLUE crawler , to het the schema of the data , saved it into an AWS crawler database 
10- Used Amazon Athena in the crawler database to run some SQL queries and gained insights 


Github Source of the project : https://github.com/datewithdata1/DE-PROJECT
