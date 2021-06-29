---
author: isaac
title: Basics in Data Engineering
---

When preparing for my data engineering interview, I realized that there are a lot of basics people may not necessarily know which require some form of revision. There are jargon like Hadoop, AWS SageMaker, PySpark, HDFS, Hive, Pig, data mart, data warehouse etc. The panel may ask you specific technical questions related to the role that you may need to prepare for. This profession is not for the unprepared/ faint of heart. So let's go through some of this so you will be more confident in talking about your skills:

1) Data Lake, Data Mart and Data Warehouse

* Try to keep the focus onb the Data Warehouse, aka a Data Hub (sometimes branded as an on premise service). Usually the DW is schema on read. This means that it forms an ETL pipeline - which stands for Extract, Transform, Load. Of course when it is loaded it is for strategic/ tactical queries with aggregation functions.
* A data mart pertains to business line/ department. If you don't have a existing data warehouse (which you porobably should have one) then you will need to resort to making a data mart. This is easier to model as it uses a star schema. However, complex transactional queries would not be useful as it would require a lot of overhead to talk to the other data marts.
* Try to not talk too much about data lake. Although, if you understand the difference between cold storage and hot storage it would be good enough. Just tell the panel what kinds of lakes you have used. E.g. Google Cloud Storage, AWS EC2. The elasticity of cloud storage has potential to optimize costs and so is making scalable containerize apps, just make sure you know how to benchmark your improvements

2) Hadoop, HDFS, Hive, Pig, MapReduce