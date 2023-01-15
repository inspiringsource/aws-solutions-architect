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

## ## CloudFormation top-level sections

* **Resources** section declares the AWS resources that you want to include in the stack. Let's add the EC2 resource to your stack.

* **Parameters** section declares the parameters that you want to use in your template. Parameters are values that you can specify when you create or update a stack. You can use parameters to customize your stack. For example, you can use parameters to specify the Amazon EC2 instance type, the Amazon EC2 key pair, or the number of Amazon EC2 instances to launch.

* **Outputs** section declares the values that you want to return when you view the stack in the AWS CloudFormation console. For example, you can return the public IP address of an Amazon EC2 instance so that you can connect to it.

* **Metadata** section declares additional information about the template. For example, you can use the Metadata section to specify the version of the template schema that you want to use.

* **Conditions** section declares conditions that you can use to customize your template. For example, you can use conditions to specify whether to create an Amazon EC2 instance in a specific Availability Zone.

* **Mappings** section declares mappings that you can use to customize your template. For example, you can use mappings to specify the Amazon Machine Image (AMI) ID for a specific Amazon EC2 instance type in a specific AWS Region.

* **Transform** section declares macros that you can use to customize your template. For example, you can use macros to specify a set of resources that you want to include in your stack.

[CloudFormation top-level sections](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html#template-anatomy-sections)

## Further Resources: 

[AWS CloudFormation Workshop](https://catalog.workshops.aws/cfn101/en-US/introduction)

[Template Walkthrough](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html)

## Youtube videos:

[What is AWS Cloudformation? Pros and Cons?](https://youtu.be/0Sh9OySCyb4)

[AWS CloudFormation Template Tutorial](https://youtu.be/_jqwVpO1w6A)