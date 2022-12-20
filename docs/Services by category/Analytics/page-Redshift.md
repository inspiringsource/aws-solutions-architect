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

## Amazon Redshift Spectrum

Amazon Redshift Spectrum is a feature of Amazon Redshift that enables you to run SQL queries on data stored in Amazon S3. With Redshift Spectrum, you can extend the data warehouse queries to read data directly from Amazon S3, without having to load the data into Amazon Redshift. This can be useful if you have large amounts of data that you want to analyze but do not want to incur the costs and time associated with loading and processing the data within Redshift.

Redshift Spectrum uses the same SQL syntax and tools as Amazon Redshift, so you can use it seamlessly with your existing Redshift workloads. Redshift Spectrum also integrates with other AWS services, such as Amazon Athena, Amazon EMR, and Amazon Glue, so you can easily analyze and transform your data using the full range of AWS analytics and data processing capabilities.

To use Redshift Spectrum, you define external tables that reference data stored in Amazon S3. When you run a query that includes these external tables, Redshift Spectrum automatically retrieves the relevant data from S3 and processes it in parallel with the rest of the query. This allows you to perform complex analytical queries on data that might not fit within the storage limits of your Amazon Redshift cluster, or to offload older, less frequently accessed data from your cluster to S3 to reduce storage costs.
## Further readings / viewing:

[Amazon Redshift Database Developer Guide](https://docs.aws.amazon.com/redshift/latest/dg/welcome.html)

[Power highly resilient use cases with Amazon Redshift](https://aws.amazon.com/blogs/big-data/power-highly-resilient-use-cases-with-amazon-redshift/)

[AWS Glue PySpark:Insert records into Amazon Redshift Table](https://youtu.be/EetkEf359QE)

