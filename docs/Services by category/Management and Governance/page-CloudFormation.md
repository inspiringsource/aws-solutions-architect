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

## Further use cases:

For example, if you want to map an Amazon Elastic Block Store volume to an Amazon EC2 instance, you reference the logical IDs to associate the block stores with the instance:

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
[Resouces](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resources-section-structure.html)

## Questions examples

As a Solution Architect, you need to build a CloudFormation template that will provision a highly available architecture. After the stack has been created you need to a convenient way to return the DNS hostname of the load balancer. Which template section would provide the DNS hostname after stack creation?        

Answer: [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)



What section of the document root must be included in an AWS CloudFormation template to include objects specified by the AWS Serverless Application Model (SAM) in addition to Resources?

```json
"Transform" : {
    "Name" : "AWS::Serverless-2016-10-31",
    "Parameters" : {
      "CodeUri" : "s3://bucket/key",
      "Function1" : {
        "CodeUri" : "s3://bucket/key",
        "Handler" : "index.handler",
        "Runtime" : "nodejs4.3"
      }
    }
  }
```
[Transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

## Further Resources: 

[AWS CloudFormation Workshop](https://catalog.workshops.aws/cfn101/en-US/introduction)

[AWS Serverless Application Model (AWS SAM)](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html)

[Learn template basics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/gettingstarted.templatebasics.html)

## Youtube videos:

[What is AWS Cloudformation? Pros and Cons?](https://youtu.be/0Sh9OySCyb4)

[AWS CloudFormation Template Tutorial](https://youtu.be/_jqwVpO1w6A)