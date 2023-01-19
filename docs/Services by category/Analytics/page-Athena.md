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

## Using workgroups to control query access and costs

Use workgroups to separate users, teams, applications, or workloads, to set limits on amount of data each query or the entire workgroup can process, and to track costs. Because workgroups act as resources, you can use resource-level identity-based policies to control access to a specific workgroup. You can also view query-related metrics in Amazon CloudWatch, control costs by configuring limits on the amount of data scanned, create thresholds, and trigger actions, such as Amazon SNS, when these thresholds are breached.

Workgroups integrate with IAM, CloudWatch, Amazon Simple Notification Service, and AWS Cost and Usage Reports as follows:

* IAM identity-based policies with resource-level permissions control who can run queries in a workgroup.

* Athena publishes the workgroup query metrics to CloudWatch, if you enable query metrics.

* In Amazon SNS, you can create Amazon SNS topics that issue alarms to specified workgroup users when data usage controls for queries in a workgroup exceed your established thresholds.

* When you tag a workgroup with a tag configured as a cost allocation tag in the Billing and Cost Management console, the costs associated with running queries in that workgroup appear in your Cost and Usage Reports with that cost allocation tag.


(AWS service integrations with Athena)[https://docs.aws.amazon.com/athena/latest/ug/athena-aws-service-integrations.html]