---
author: isaac
title: Basics in Data Engineering
---

When preparing for my data engineering interview, I realized that there are a lot of basics people may not necessarily know which require some form of revision. There are jargon like Hadoop, AWS SageMaker, PySpark, HDFS, Hive, Pig, data mart, data warehouse etc. The panel may ask you specific technical questions related to the role that you may need to prepare for. This profession is not for the unprepared/ faint of heart. So let's go through some of this so you will be more confident in talking about your skills:

0. Data Lake, Data Mart and Data Warehouse

    * Try to keep the focus on the Data Warehouse, aka a Data Hub (sometimes branded as an on premise service). Usually the DW is schema on read. This means that it forms an ETL pipeline - which stands for Extract, Transform, Load. Of course when it is loaded it is for strategic/ tactical queries with aggregation functions.
    * A data mart pertains to business line/ department. If you don't have an existing data warehouse (which you porobably should have one) then you will need to resort to making a data mart. This is easier to model as it uses a star schema. However, complex transactional queries would not be useful as it would require a lot of overhead to talk to the other data marts.
    * Try to not talk too much about data lake. Although, if you understand the difference between cold storage and hot storage it would be good enough. Just tell the panel what kinds of lakes you have used. E.g. Google Cloud Storage, AWS EC2. The elasticity of cloud storage has potential to optimize costs and so is making scalable containerize apps, just make sure you know how to benchmark your improvements

1. Hadoop, HDFS, Hive, Pig, MapReduce, Impala

    * The list of words above aren't that complicated. Hadoop is simply a collection of modules created in Java programming language. Hadoop facilitates a software framework for distributed storage and the processing of big data using the MapReduce Programming Model
    * MapReduce --> literally map and reduce. MapReduce is known for locally processing the data at the nodes. So local data is 'mapped' onto temp storage. Then, Worker nodes redistribute the data among the nodes so that keys are sorted. Reduce --> meaning duplicates are removed
    * MapReduce works on use cases such as common Facebook friends. You can see how it applies as the parallelized map function only happens in the local mcahine. Whereas the shuffle and reduce is a form of distributed computing.
    * MapReduce is useful for large datasets (in the petabytes) and good if the durability as failovers cause the work to be rescheduled.
    * How are these tasks being tracked or scheduled? Easy. Thats where the HDFS comes in.
    * HDFS --> Hadoop Distributed File System. HDFS is for storing and MapReduce for processing. It consists of
    * Name Node: Also called the Master Node. Basically it tracks the slave daemons and checks whether they are still alive
    * Data Node: The slave daemons. Sends a heartbeat every 3 seconds to Name Node to convey it is still alive.
    * Job Tracker: Receives the MapReduce requests from the client and talks to the Name Node to know about location of processing
    * Task Tracker: Salve of the Job Tracker
    * Pig: It's basically MapReduce but written in high level procedural language: Pig Latin. Using this can help data processing procedures without needing to import the data into a database first. It represents a directed acyclic graph (DAG) rather than pipeline. SQL, on the other hand, is declarative, it orients itself around queries with a single result. Pig orients itself around a execution plan.
    * Hive provides high level abstraction of SQL-like queries in the form of HiveQL without need for implemention of low-level Java API. Contains:
    * Metastore: Basically tracking metadata in the form of RDBMS
    * Driver: Tracks the commands in the CLI and execution sessions
    * Spark --> provides an interface for programming entire clusters with implicit data parallelism and fault tolerance.

2. Data warehouses - Hive-QL, Snowflake ANSI, RedShift SQL

    * You should know that almost all databases have some form of proprietary SQL. Simplicity and complexity therefore, may vary.
    * Snowflake uses the most common standardized version: SQL ANSI (American National Standards Institute)
    * Redshift SQL: Based on PostgreSQL. specifically designed for OLAP and BI applications, which require complex queries against large datasets. Therefore, unlike OLTP that stores data in rows, Redshift stores data in columns for optimum memory usage.

3. Amazon EMR, Glue, Athena, Data Pipeline, Lambda, SageMaker

    * EMR --> similar to Hadoop, provides control in provisioning capacity and tuning clusters
    * Glue --> serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
    * Athena --> Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.
    * Lambda --> AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes.

4. DevOps, CI/CD

    * Only go into this if you have extensive experience
    * DevOps has different concepts than Agile, although it is similar.
    * CI --> Continuious Integration is based on CD --> Continuous Development/ Deployment
    * If you want to achieve a culture of DevOps , see some tips [here](https://en.wikipedia.org/wiki/Continuous_delivery) (hop to the section on strategies)
    * Selling CD as a painkiller: Many people don't want to hear a whole rationale of why they should change their culture. It could be fear of change, it could be lack of understanding of new approaches and the value in investing in the approach. Don't educate, sell a solution.
    * Having multidisciplinary members: Don't be afraid to branch out and learn a new skill. Employers like that. Lack of adoption of a holistic approach could be due to incompetence
    * Continuous delivery of continuous delivery: You **need** to justify concrete benefits along the way while emphasizing the effects of CD so that you achieve buy-in from your stakeholders/ managers
    * Always start with easy but important applications: Choose first use cases that are easy to migrate and that are important to the business. You don't want to request something from the stakeholder that would cut off the relationship but accept a change as a positive thing
    * Visual CD pipeline skeleton --> This is great advice, especially if your team doesn't have an Agile culture ATM and you want to affect change. A CD pipeline skeleton can simply be a progressive map on what kind of problems you see with the SDLC of the company and the kinds of problems you can solve from a SDLC standpoint. When you have 3 or 4 different ideas to help the solution of a potential improvement in the SDLC, use that idea first. Similarly, you can have a Data Strategy documentation of problems and stakeholders in the company, and identify the best project for the highest ROI. This gives you a better way to provide a hypothetical data use case as a proposal before the approval stages. It also provides a concreate understanding of your thought process to persuade your manager that you have a high level view of this.
    * Expert drop --> simply means getting an expert consultant to support change management. Personally, I'd rather be that change agent.
