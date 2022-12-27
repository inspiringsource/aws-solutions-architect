---
title: AWS CloudFormation
description: Lorem ipsum dolor sit amet - 2
---

AWS CloudFormation is a web service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you.

## AWS CloudFormation templates

AWS CloudFormation to automate the deployment of the Disaster Recovery for AWS IoT in the AWS Cloud. It includes templates, which you can deploy the solution as such in the primary and secondary Regions. [Source](https://docs.aws.amazon.com/solutions/latest/disaster-recovery-for-aws-iot/aws-cloudformation-templates.html)

## Sample templates

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
- Metadata: [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)

- Parameters: [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)

- Rules: [Rules](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/rules-section-structure.html)

- Mappings: [Mappings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html)

- Conditions: [Conditions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/conditions-section-structure.html)

- Transform: [Transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)

- Resources: [Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resources-section-structure.html)

- Outputs: *can returns the DNS name for the resource with the logical ID* [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)

[Template anatomy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)

[Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/sample-templates-services-us-west-2.html)

Further use cases:

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