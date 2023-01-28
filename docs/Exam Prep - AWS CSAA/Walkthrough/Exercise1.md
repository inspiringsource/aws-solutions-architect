---
title: "Exercise 1: Testing Permissions"
---
Exercise 1: Testing Permissions involve creating and configuring various AWS resources to create a Lambda function that will upload a file to an S3 bucket and insert an item into a DynamoDB table. It includes creating an S3 bucket and DynamoDB table, noting an existing IAM role, creating a policy for the S3 bucket, creating a Lambda function, and verifying that the file was uploaded and the item was inserted. exercise was taken from [Week 1 Exercise](https://www.coursera.org/learn/aws-certified-solutions-architect-associate/supplement/Yvk1o/lab-exercise-testing-permissions) course.

## Task 1: Creating an S3 bucket

1. Log in to the AWS Management Console and navigate to the S3 service.
2. Click on the "Create Bucket" button.
3. Enter a unique name for the bucket in the "Bucket Name" field. Make sure to follow the naming conventions for S3 bucket names.
4. Choose the region you want to create the bucket in. It's the value of the Region located to the left of these instructions.
5. Click on the "Create" button to create the bucket.
6. Make a note of this bucket name because you will need it later.

## Task 2: Creating a DynamoDB table

1. Log in to the AWS Management Console and navigate to the DynamoDB service.
2. Click on the "Create table" button.
3. Enter a unique name for the table in the "Table name" field.
In the "Primary key" section, enter `ID` as the partition key.
4. Choose the region you want to create the table in. It's the value of the Region located to the left of these instructions.
5. Click on the "Create" button to create the table.
6. Make a note of this table name because you will be needed later.
## Task 3: Noting the existing IAM Role

1. Log in to the AWS Management Console and navigate to the IAM service.
2. Select "Roles" from the navigation menu on the left.
3. Search for the role `LabLambdaRole` and click on it.
4. On the role summary page, find the Amazon Resource Name (ARN) and make a note of it.
## Task 4: Creating an S3 bucket policy

1. Log in to the AWS Management Console and navigate to the S3 service.
2. Find the S3 bucket that you created earlier and click on it.
3. In the "Permissions" tab, click on the "Bucket Policy" button.
4. Use the policy generator to create a policy that grants the `LabLambdaRole` access to the S3 bucket.
5. Choose the region you want to create the policy in. It's the value of the Region located to the left of these instructions.
6. Click on the "Save" button to save the policy.
## Task 5: Creating a Lambda function

1. Log in to the AWS Management Console and navigate to the Lambda service.
2. Click on the "Create function" button.
3. Select the "Author from scratch" option.
4. Enter a unique name for the function in the "Function name" field.
5. Choose "Python 3.9" as the runtime.
6. In the "Permissions" section, choose the `LabLambdaRole` as the existing role.
7. Choose the region you want to create the function in. It's the value of the Region located to the left of these instructions.
8. Click on the "Create function" button.
9. In the "Environment variables" section, create two environment variables: `DYNAMODB_TABLE_NAME` and `S3_BUCKET_NAME`.
10. Enter the value of your DynamoDB table name and S3 bucket name respectively.
11. In the "Function code" section, paste the code provided above
12. Click on the "Deploy" button to deploy the function.
13. Test your function

```python
import os
import boto3
import uuid
s3 = boto3.resource('s3')
dynamodb = boto3.resource('dynamodb')
def lambda_handler(event, context):
   message = "Hello from AWS Lambda!"
   encoded_string = message.encode("utf-8")
   file_name = "hello.txt"
   s3_path = "test/" + file_name
   dynamodb.Table(os.environ['DYNAMODB_TABLE_NAME']).put_item(Item={'ID': '12345','content':message})
   s3.Bucket(os.environ['S3_BUCKET_NAME']).put_object(Key=s3_path, Body=encoded_string)
   response = {
      'statusCode': 200,
      'body': 'success!',
      'headers': {
            'Content-Type': 'application/json',
            'Access-Control-Allow-Origin': '*'
      },
   }
   return response
```

## Task 6: Verifying the object

Verify that the object was uploaded to the S3 bucket and inserted into the DynamoDB table.