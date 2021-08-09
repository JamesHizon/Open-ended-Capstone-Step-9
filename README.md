# Open-ended Capstone Step-9: Deploy Production Code & Process Dataset

### Description
In this step of my capstone project, I had to deploy my code optimized in the previous step (after writing unit tests) towards a fresh set of AWS compute resources. I basically created a new S3 Bucket, and had to create new EMR Clusters. I realized after the second time, that I may need to adjust configuration settings for Cluster creation so that I would not need to continually spend time terminating and cloning a new EMR Cluster and stopping the EMR Notebook from running.

### Issue on AWS Redshift via AWS Educate account
Given the AWS Educate account, I was unable to work directly with AWS Redshift as a data warehouse solution, so I mainly just used AWS S3 as a Data Lake solution that also stored data that was being transformed in two separate file folders. S3 has a decent storage capacity, so I mainly just dealt with S3, but tried to take note of other options for data storage such as AWS RDS and Redshift.

### Athena and Glue
I was advised to work with Athena and Glue by previous mentor to learn about automatic schema and table creation. Because of the two file folders that I created to store transformed data, I was able to automatically figure out the schema and write a simple query on that table. The two tables contained all data from files. It helped me to figure out and see that it may be crucial to not drop the "DATE" column so I can query by date for further analysis later on. As a result of the automatic schema creation, it also enabled me to see that I do not need to use Spark to alter the data types.

### Files
1. Jupyter Notebook file used to extract, load and process data.
2. Screenshot of S3 bucket (prior to processing data).
3. Screenshot of using Glue and Athena to automatically create schema and tables of two separate file folders.
