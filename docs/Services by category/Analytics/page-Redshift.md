---
title: Amazon Redshift
description: Fastest, easiest, and most widely used cloud data warehouse
---
<div>
<div align="center"><img src={require('@site/static/img/shift-away.png').default} /></div>
</div>
<br/>
<div><h3 align="center">"Warehousing service that houses analytical data for use in complex queries, *BI reporting, and *ML."</h3></div>

<p align="right">*Business Intelligence tools<br/> 
*Redshift Machine Learning
</p>


Amazon Redshift uses SQL to analyze structured and semi-structured data. It is designed to handle the most demanding workloads, including data warehouses, data lakes, and advanced analytics. 
## Cloud data warehouse

Amazon Redshift is a fully managed, petabyte-scale data **warehouse** service in the cloud. You can start with just a few hundred gigabytes of data and scale to a petabyte or more. Your data warehouse is always available, with fast query performance and no capacity planning or management required. You can use your existing business intelligence (BI) tools and dashboards to analyze your data in Amazon Redshift.

## Typical data processing flow for Amazon Redshift

![Typical data processing flow for Amazon Redshift](https://docs.aws.amazon.com/images/redshift/latest/gsg/images/architecture.png)

## Good for

- Data warehousing
- Data lakes
- Advanced analytics
- Business intelligence (BI) tools and dashboards

## Not good for

- Data processing
- Data storage
- Data streaming

## &#9888 Important

Column-oriented databases are not good for data processing. They are good for data warehousing, data lakes, and advanced analytics.
* Data is indexed using columnar indexing        
* Queries execute parallel across all nodes        
* You can query Amazon S3 without moving data to Amazon Redshift        

Amazon Redshift clusters support only availability zone (Single-AZ).

By default, Amazon Redshift has excellent tools to back up your cluster via snapshot to Amazon S3. However, you can also use AWS Backup to back up your Amazon Redshift cluster. Source: [Building Multi-AZ or Multi-Region Amazon Redshift Clusters](https://aws.amazon.com/blogs/big-data/building-multi-az-or-multi-region-amazon-redshift-clusters/)

## Further readings / viewing:

[Amazon Redshift Database Developer Guide](https://docs.aws.amazon.com/redshift/latest/dg/welcome.html)

[Power highly resilient use cases with Amazon Redshift](https://aws.amazon.com/blogs/big-data/power-highly-resilient-use-cases-with-amazon-redshift/)

[AWS Glue PySpark:Insert records into Amazon Redshift Table](https://youtu.be/EetkEf359QE)

