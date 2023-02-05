---
title: "Exercise 3: Comparing Databases"
---

Exercise 3: Comparing Databases will take you through the process of launching an RDS instance in the specified region, create a read replica for it, create a DynamoDB table, and enable DAX by providing necessary information in the AWS Management Console for each service.

## Task 1: Launching an RDS instance

1. Log in to the AWS Management Console.
2. Go to the RDS service.
3. Click on the "Launch a DB instance" button.
4. Select "MySQL" as the engine.
5. Choose the "Standard create" option.
6. Select the desired instance class (either "db.t2.micro" or "db.t3.micro").
7. Choose the VPC "Lab VPC" for your RDS instance.
8. Use the value of the "Region" located to the left of these instructions as the region for 1. your RDS instance.
9. Fill in the remaining required fields, such as the DB instance identifier, master username, and password.
10. Click on the "Launch DB Instance" button to launch your RDS instance.

## Task 2: Creating a read replica

1. Go to the RDS service.
2. Click the RDS instance for which you want to create a read replica.
(wait for the instance Status to change to "Available". This might take a few minutes...)
3. Click on the "Instance actions" button and select "Create read replica".
4. Fill in the "DB instance identifier" with a unique identifier.
5. Use the value of the "Region" located to the left of these instructions as the region for the read replica.
6. Fill in the remaining required fields.
7. Click on the "Create read replica" button to create a read replica.

## Task 3: Creating a DynamoDB table

1. Go to the DynamoDB service.
2. Click on the "Create table" button.
3. Fill in the "Table name" with a unique name.
4. Fill in the "Partition key" with a unique key name.
5. Fill in the remaining required fields.
6. Click on the "Create" button to create the DynamoDB table.

## Task 4: Enabling DAX

1. Go to the DynamoDB service.
2. Click on the "Tables" tab.
3. Locate the table for which you want to enable DAX.
4. Click on the "Actions" button and select "Manage DAX cluster".
5. Click on the "Create DAX cluster" button.
6. Fill in the "Node type" with "dax.r5.large".
7. Fill in the "Number of nodes" with "3".
8. Choose "Create new" for the subnet.
9. Choose the "Lab VPC" for the VPC ID.
10. Choose the "LabDXRole" for the IAM service role.
11. Fill in the remaining required fields.
12. Click on the "Create DAX cluster" button to create the DAX cluster.