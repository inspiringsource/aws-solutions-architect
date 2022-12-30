---
title: Amazon Route 53
description: Lorem ipsum dolor sit amet - 2
---

Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. You can use Route 53 to perform three main functions in any combination: domain registration, DNS routing, and health checking.

If you choose to use Route 53 for all three functions, be sure to follow the order below:

1. Register domain names
Your website needs a name, such as example.com. Route 53 lets you register a name for your website or web application, known as a domain name.

For an overview, see How domain registration works.

For a procedure, see Registering a new domain.

For a tutorial that takes you through registering a domain and creating a simple website in an Amazon S3 bucket, see Getting started with Amazon Route 53.

2. Route internet traffic to the resources for your domain
When a user opens a web browser and enters your domain name (example.com) or subdomain name (acme.example.com) in the address bar, Route 53 helps connect the browser with your website or web application.

For an overview, see How internet traffic is routed to your website or web application.

For procedures, see Configuring Amazon Route 53 as your DNS service.

For a procedure on how to route email to Amazon WorkMail, see Routing traffic to Amazon WorkMail.

3. Check the health of your resources
Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functional. You also can choose to receive notifications when a resource becomes unavailable and choose to route internet traffic away from unhealthy resources.

## Amazon Route 53 in a nutshell

Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like


Route 53's new DNS Failover feature gives you the power to monitor your website and automatically route your visitors to a backup site if it goes down. DNS Failover pairs up well with Amazon S3s website hosting feature to create a simple, low-cost, and reliable way to deploy a backup website.


## Sources:

[What is Amazon Route 53?](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html)

[How do I configure my website to fail over to an S3 bucket when a Route 53 health check fails?](https://aws.amazon.com/premiumsupport/knowledge-center/fail-over-s3-r53/)

[Create a Backup Website Using Route 53 DNS Failover and S3 Website Hosting 2014](https://aws.amazon.com/blogs/aws/create-a-backup-website-using-route-53-dns-failover-and-s3-website-hosting/)