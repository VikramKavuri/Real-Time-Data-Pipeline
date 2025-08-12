# Snowflake-Kinesis-Airflow-Big-Data-Project

I created an end-to-end data pipeline for this big data project utilizing Snowflake, AWS Services, and Apache Airflow to schedule all of the activity.

# Data Architecture

The aws-kinesis-agent was installed on an Amazon EC2 instance. The streaming data was subsequently transferred to
an Amazon S3 bucket through the AWS kinesis firehose delivery stream.
In the bucket, I divided the space into three zones: Landing, Processing, and Processed using Airflow DAG. After the data was ingested and modified, Snowflake Datawarehouse was used to store the results.

# AWS Service Used

- IAM
- S3
- EC2
- Kinesis Firehose
- Cloud Watch
- Kinesis Agent
- AWS Managed Airflow(MWAA)

# Side Note

- I used Airflow in this project instead of Snow Pipe because of the drawback of Snow Pipe in which ordering is not guarantee.
- Created a storage integration on snowflake to avoid exposing my secret and access key on my github repository.
- Troubleshoot my Dag in Airflow to fix some error message
