# Building a Spark Data pipeline with Delta Lake

 We are implementing a *medallion / multi-hop* architecture by using Delta Lake which is's a OSS standard that brings SQL Transactional database capabilities on top of parquet files.
we are using Spark format, built on top of Spark API / SQL that allows ACID transactionns, DML operations,streaming and batch support,time travel and performance boots by Zordering to 
solve for smaller files. The goal here is to build a solution that reduces customers churn with Databricks Lakehouse. 
Analyse and explain current customer churn quantify churn, trends and the impact for the business.
#### Introduction - Raw Data
1.  Ingest source data from  Customer profiles coming from our website, order details from our ERP system and mobile application clickstream to analyse our customers activity.
2.  Secure data as table  and grant read access to the Data Analyst and Data Science teams.
3.  Raw data includes Customer profile data, Orders history and events(streaming data)
4.  ordersFolder = rawDataVolume + '/orders'
    usersFolder = rawDataVolume + '/users'
    eventsFolder = rawDataVolume + '/events'
5. Load with Autoloader
   
 #### Data Engineering
 1.  Build a Spark Data Pipeline with Delta Lake using notebooks
 2.  Configure cluster for note book
 3.  Check the volume Unity catalog (data governance)
 4.  Read the jason raw data : display(spark.sql("SELECT * FROM json.`"+rawDataVolume+"/users`"))
 5.  Read CSV into a dataframe : df = spark.read.option("header", "true").csv(rawDataVolume + "/events")
 6.  Display using Spark SQL : display(spark.sql("SELECT * FROM eventsView"))
 7.  Load data using Databricks Autoloader ( efficiently ingest millions of files from a cloud storage, and support efficient schema inference and evolution at scale both Jason and CVS files)
 8.  Creating "Bronze" Delta table using spark.readStream + writeStream. Read contents of Bronze table using spark %sql  select * from churn_users_bronze
 9.  Optimize the tables using (Z Order)

























      
