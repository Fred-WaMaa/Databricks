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
 1.  Build a Spark Data Pipeline with Delta Lake
 2.  
