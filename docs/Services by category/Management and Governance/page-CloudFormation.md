---
title: AWS CloudFormation
description: Lorem ipsum dolor sit amet - 2
---

AWS CloudFormation is a web service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you.

## AWS CloudFormation templates

AWS CloudFormation to automate the deployment of the Disaster Recovery for AWS IoT in the AWS Cloud. It includes templates, which you can deploy the solution as such in the primary and secondary Regions. [Source](https://docs.aws.amazon.com/solutions/latest/disaster-recovery-for-aws-iot/aws-cloudformation-templates.html)

## Template anatomy

The following sample templates are provided for you to use as a starting point for your own templates. 


```json
{
  "AWSTemplateFormatVersion" : "version date",

  "Description" : "JSON string",

  "Metadata" : {
    template metadata
  },

  "Parameters" : {
    set of parameters
  },
  
  "Rules" : {
    set of rules
  },

  "Mappings" : {
    set of mappings
  },

  "Conditions" : {
    set of conditions
  },

  "Transform" : {
    set of transforms
  },

  "Resources" : {
    set of resources
  },
  
  "Outputs" : {
    set of outputs
  }
}

```
[template-anatomy-sections-explained](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html#template-anatomy-sections)

## CloudFormation top-level sections

* **Resources** *(required)* section declares the AWS resources that you want to include in the stack. For example, you can declare an Amazon EC2 instance, an Amazon RDS DB instance, or an Amazon S3 bucket. 

Resource properties are additional options that you can specify for a resource. For example, for each EC2 instance, you must specify an Amazon Machine Image (AMI) ID for that instance. You declare the AMI ID as a property of the instance, as shown in the following example:

  ```json
"Resources" : {
  "MyEC2Instance" : {
    "Type" : "AWS::EC2::Instance",
    "Properties" : {
      "ImageId" : "ami-0ff8a91507f77f867"
    }
  }
}  
  ```

* **Parameters** *(optional)* section declares the parameters that you want to use in your template. Parameters are values that you can specify when you create or update a stack. You can use parameters to customize your stack. For example, you can use parameters to specify the Amazon EC2 instance type, the Amazon EC2 key pair, or the number of Amazon EC2 instances to launch.

* **Outputs** *(optional)* section declares the values that you want to return when you view the stack in the AWS CloudFormation console. For example, you can return the public IP address of an Amazon EC2 instance so that you can connect to it. 

In the following example, the output named BackupLoadBalancerDNSName returns the DNS name for the resource with the logical ID BackupLoadBalancer only when the CreateProdResources condition is true. (The second output shows how to specify multiple outputs.)
  
  ```json
"Outputs" : {
  "BackupLoadBalancerDNSName" : {
    "Description": "The DNSName of the backup load balancer",  
    "Value" : { "Fn::GetAtt" : [ "BackupLoadBalancer", "DNSName" ]},
    "Condition" : "CreateProdResources"
  },
  "InstanceID" : {
    "Description": "The Instance ID",  
    "Value" : { "Ref" : "EC2Instance" }
  }
}    
  ```

* **Metadata** *(optional)* section declares additional information about the template. For example, you can use the Metadata section to specify the version of the template schema that you want to use.

* **Conditions** *(optional)* section declares conditions that you can use to customize your template. For example, you can use conditions to specify whether to create an Amazon EC2 instance in a specific Availability Zone.

* **Mappings** *(optional)* section declares mappings that you can use to customize your template. For example, you can use mappings to specify the Amazon Machine Image (AMI) ID for a specific Amazon EC2 instance type in a specific AWS Region.

The following example shows a Mappings section with a map RegionMap, which contains five keys that map to name-value pairs containing single string values. The keys are region names. Each name-value pair is the AMI ID for the HVM64 AMI in the region represented by the key.

The name-value pairs have a name (HVM64 in the example) and a value. By naming the values, you can map more than one set of values to a key.

  ```json
"Mappings" : {
  "RegionMap" : {
    "us-east-1"      : { "HVM64" : "ami-0ff8a91507f77f867"},
    "us-west-1"      : { "HVM64" : "ami-0bdb828fd58c52235"},
    "eu-west-1"      : { "HVM64" : "ami-047bb4163c506cd98"},
    "ap-southeast-1" : { "HVM64" : "ami-08569b978cc4dfa10"},
    "ap-northeast-1" : { "HVM64" : "ami-06cd52961ce9f0d85"}
  }
}   
  ```

* **Transform** section declares macros that you can use to customize your template. For example, you can use macros to specify a set of resources that you want to include in your stack.

[CloudFormation top-level sections](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html#template-anatomy-sections)

## Further Resources: 

[AWS CloudFormation Workshop](https://catalog.workshops.aws/cfn101/en-US/introduction)

[Template Walkthrough](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html)

## Youtube videos:

[What is AWS Cloudformation? Pros and Cons?](https://youtu.be/0Sh9OySCyb4)

[AWS CloudFormation Template Tutorial](https://youtu.be/_jqwVpO1w6A)