---
title: Amazon RDS
---

<div><h3 align="center">"Scale a relational database in the cloud with just a few clicks."</h3></div>

Amazon Relational Database Service (RDS) is a web service that makes it easier to set up, operate, and scale a relational database in the cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks, freeing up developers to focus on what makes their applications and businesses unique.

## RDS is a managed service

RDS is a managed service, which means Amazon takes care of patching, backups, and maintenance for you. You can use RDS to deploy and scale popular database engines like MySQL, PostgreSQL, MariaDB, Oracle, Microsoft SQL Server, and Amazon Aurora. You can also use RDS to deploy and scale a database in the cloud that is compatible with your existing on-premises applications.

## RDS Multi AZ vs Read Replicas

RDS Multi AZ is a feature that provides high availability for your database. It automatically creates a synchronous standby replica in another Availability Zone (AZ) for your primary database. If the primary database fails, Amazon RDS automatically promotes the standby replica to be the new primary database. You can use Multi AZ to help protect your database from hardware failure, planned maintenance, and other disruptions. Multi AZ is available for MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server.

Read Replicas are a feature that provides read scalability for your database. You can create up to 15 read replicas of your primary database. Read replicas are available for MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server. You can use read replicas to offload read-only workloads from your primary database. You can also use read replicas to help protect your database from hardware failure, planned maintenance, and other disruptions.

[Read more](https://aws.amazon.com/about-aws/whats-new/2018/01/amazon-rds-read-replicas-now-support-multi-az-deployments/)


## Working with parameter groups

Parameter groups are a collection of parameters that control the behavior of the database engine. You can create and modify parameter groups to change the behavior of your database. For example, you can use parameter groups to change the default character set for your database.

Working with parameter groups is a common task when working with RDS. You can use the AWS CLI, AWS SDKs, or the AWS Management Console to create and modify parameter groups. Read more about [working with parameter groups](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithParamGroups.html).