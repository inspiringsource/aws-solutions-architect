---
title: Amazon Athena
description: serverless analyzing data in S3 using  SQL
---
<h3 align="center">"A query service to analyze data in Amazon S3 using standard SQL."</h3>


Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.   

Athena is easy to use. Simply point to your data in Amazon S3, define the schema, and start querying using standard SQL. Most results are delivered within seconds. With Athena, there’s no need for complex extract, transform, and load (ETL) jobs to prepare your data for analysis. This makes it easy for anyone with SQL skills to quickly analyze large-scale datasets.
  

Athena is out-of-the-box integrated with AWS Glue Data Catalog, allowing you to create a unified metadata repository across various services, crawl data sources to discover schemas and populate your Catalog with new and modified table and partition definitions, and maintain schema versioning.


<div>
<div align="center"><img src={require('@site/static/img/Amazon-Athena.png').default} /></div>
<div><p align="center">Athena is out-of-the-box integrated with <a href="page-Glue">AWS Glue</a></p></div>
</div>

## Amazon Athena is serverless

Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run

Immediately start querying using the built-in query editor. You can also use AWS Glue to automatically crawl data sources to discover data and populate your Data Catalog. Results are displayed in the console within seconds, and automatically stored in S3.


