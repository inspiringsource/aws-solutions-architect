---
title: AWS Backup
description: Manage and automate data protection
---

AWS Backup is a fully managed backup service that makes it easy to centralize and automate the backup of data across AWS services. AWS Backup simplifies data protection for Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Relational Database Service (Amazon RDS) databases, and Amazon DynamoDB tables. You can use AWS Backup to back up your data to Amazon Simple Storage Service (Amazon S3) and Amazon Glacier, and restore data from backups to Amazon EC2 instances, Amazon RDS databases, and Amazon DynamoDB tables.

<div>
<div align="center"><img src="https://d1.awsstatic.com/aws-storage/AWS-Backup-AWS-Geek-Diagram.07903cab8f9f4b31d5ca2dce4fd2a9c936ff93b9.jpg" /></div>
<div><p align="center">Diagram Source: <a href="https://aws.amazon.com/backup/resources/?nc=sn&loc=5&refid=60b4082c-a1a5-4bfd-b520-7f3ab404cbd5&backup-blogs.sort-by=item.additionalFields.createdDate&backup-blogs.sort-order=desc">AWS Backup</a>
</p></div>
</div>

AWS Backup is a fully managed service that makes it easy to centralize and automate the backup of data across AWS services. It enables you to define backup policies and schedules for your resources, and recover them when needed.

There are different requirements for backup and recovery depending on the type of data and the specific service you are using. Here are a few examples:

<div class="table-contents"><table id="w129aab5c11b5"><thead>
          <tr>
            <th>AWS Backup supports</th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/cross-region-backup.html">Cross-Region
                backup</a></th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/create-cross-account-backup.html">Cross-account
                backup</a></th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/aws-backup-audit-manager.html">AWS Backup Audit
                Manager</a></th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/about-backup-plans.html">Incremental
              backup</a></th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/point-in-time-recovery.html">Continuous backup and
                point-in-time restore (PITR)</a></th>
            <th><a href="#full-management">Full AWS Backup management</a></th>
            <th><a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/creating-a-backup-plan.html#plan-options-and-configuration"> Lifecycle to cold storage</a></th>
            <th>Item-level restore‡</th>
          </tr>
        </thead>
          <tbody><tr>
            <td>EC2</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>S3</td>
            <td>✓^</td>
            <td>✓^</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
          </tr>
          <tr>
            <td>EBS</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>RDS</td>
            <td>✓*</td>
            <td>✓*</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>Aurora</td>
            <td>✓*</td>
            <td>✓*</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>EFS</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
          </tr>
          <tr>
            <td>FSx for Lustre</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>FSx for Windows File Server</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>FSx for ONTAP</td>
            <td></td>
            <td></td>
            <td>✓†</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>FSx for OpenZFS</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>Storage Gateway</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>DocumentDB</td>
            <td>✓*</td>
            <td>✓*</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>Neptune</td>
            <td>✓*</td>
            <td>✓*</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>Amazon Redshift</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
          </tr>
          <tr>
            <td>Amazon Timestream</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
          </tr>
          <tr>
            <td>Windows VSS</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>Virtual machines</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
          </tr>
          <tr>
            <td>AWS CloudFormation</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
          </tr>
          <tr>
            <td>DynamoDB without <a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/advanced-ddb-backup.html">AWS Backup advanced
                features</a></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>DynamoDB with <a href="https://docs.aws.amazon.com/aws-backup/latest/devguide/advanced-ddb-backup.html">AWS Backup advanced
                features</a></td>
            <td>✓</td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
          </tr>
        </tbody></table>
</div>

> ^ Destination copies from S3 buckets and RDS databases with PITR are not Point-in-Time restorable (PITR).     
> \* RDS, Aurora, DocumentDB, and Neptune do not support a single copy action that performs both cross-Region AND cross-account backup. You can choose one or the other. You can also use a AWS Lambda script to listen for the completion of your first copy, perform your second copy, then delete the first copy.       
>† AWS Backup Audit Manager supports this resource across all controls except cross-account copy and cross-Region copy.       

Source: [What is AWS Backup?](https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html)

These are all examples of databases or/and storage solutions services that can be backed up using AWS Backup with a point-in-time copy of the data that can be restored to the original service or to a different service.

Regarding the backup strategies, there are two main strategies:

1. Periodic: This strategy involves taking backups of your data at regular intervals, for example, daily or weekly. This strategy is typically used for data that does not change frequently.

2. Continuous: This strategy involves taking backups of your data continuously, as soon as it is modified. This strategy is typically used for data that changes frequently.

The RPO (Recovery Point Objective) is the maximum amount of data loss that is acceptable for a specific strategy, and the RTO (Recovery Time Objective) is the maximum amount of time within which the data must be recovered.

For example, the Periodic strategy has an RPO of 24 hours and an RTO of 24 hours, meaning that the data can lose up to 24 hours' worth of changes, but it must be recovered within 24 hours. The Continuous strategy has an RPO of 15 minutes and an RTO of 15 minutes, meaning that the data can lose up to 15 minutes worth of changes, but it must be recovered within 15 minutes.

Check out the [Disaster recovery](../../Personal-notes/Disaster_Recovery.md) page for more information.

Also, check out the [S3 Cross Region Replication (CRR)](./page-S3#replicating-objects) page for more information.

To do:
- [x] [ebook](https://d1.awsstatic.com/analyst-reports/AWS_eBookB&R_4-28-20_CA.pdf)  
- [x] review [tutorials](https://aws.amazon.com/backup/resources/?refid=60b4082c-a1a5-4bfd-b520-7f3ab404cbd5#Tutorials)  
- [x] Lab
