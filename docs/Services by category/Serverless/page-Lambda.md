---
title: AWS Lambda
description: Lorem ipsum dolor sit amet - 2
---

Lambda is a compute service that lets you run code without provisioning or managing servers. Lambda runs your code on a high-availability compute infrastructure and performs all of the administration of the compute resources, including server and operating system maintenance, capacity provisioning and automatic scaling, and logging. With Lambda, you can run code for virtually any type of application or backend service. All you need to do is supply your code.

## Particular important for the exam

> Lambda has a 15-minute timeout! Use Fargate for longer-running processes. [Source](https://aws.amazon.com/blogs/architecture/rate-limiting-strategies-for-serverless-applications/)

> Lambda is a managed service, so you don't have to worry about the underlying infrastructure. [Source](https://aws.amazon.com/lambda/faqs/)

> AWS Lambda supports Java, Go, PowerShell, Node.js, C#, Python, and Ruby code, and provides a Runtime API which allows you to use any additional programming languages to author your functions. Please read our documentation on using Node.js, Python, Java, Ruby, C#, Go, and PowerShell. [Source](https://aws.amazon.com/lambda/faqs/)

> Lambda manages the function's asynchronous event queue and attempts to retry on errors. If the function returns an error, Lambda attempts to run it two more times, with a one-minute wait between the first two attempts, and two minutes between the second and third attempts. if the function fails three times, Lambda stops invoking it. [Source](https://aws.amazon.com/lambda/faqs/)