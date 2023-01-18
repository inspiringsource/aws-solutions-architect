---
title: AWS OpsWorks
---

## What is AWS OpsWorks?

AWS OpsWorks is a configuration management service that helps you configure and operate applications in a cloud enterprise by using Puppet or Chef. AWS OpsWorks Stacks and AWS OpsWorks for Chef Automate let you use Chef cookbooks and solutions for configuration management, while OpsWorks for Puppet Enterprise lets you configure a Puppet Enterprise master server in AWS. Puppet offers a set of tools for enforcing the desired state of your infrastructure, and automating on-demand tasks. 

Chef is a configuration management tool that lets you automate the deployment of applications and infrastructure. Chef cookbooks are recipes that define the desired state of your infrastructure. OpsWorks for Chef Automate is a Chef Enterprise solution that lets you manage Chef cookbooks and automate the deployment of your infrastructure.

### Quick example of how OpsWorks works:

1. You create a stack in OpsWorks.
2. You add layers to the stack, such as a web server layer, a database layer, and an application server layer.
3. You add instances to each layer.
4. You add recipes to each layer.
5. You add custom cookbooks to the stack.
6. You deploy the stack.


## What is AWS OpsWorks Stacks?

AWS OpsWorks Stacks lets you manage applications and servers on AWS and on-premises. With OpsWorks Stacks, you can model your application as a stack containing different layers, such as load balancing, database, and application server. You can deploy and configure Amazon EC2 instances in each layer or connect other resources such as Amazon RDS databases. OpsWorks Stacks lets you set automatic scaling for your servers based on preset schedules or in response to changing traffic levels, and it uses lifecycle hooks to orchestrate changes as your environment scales. You run Chef recipes using Chef Solo, allowing you to automate tasks such as installing packages and programming languages or frameworks, configuring software, and more.

## Reference

[AWS OpsWorks User Guide](https://docs.aws.amazon.com/opsworks/latest/userguide/welcome.html)