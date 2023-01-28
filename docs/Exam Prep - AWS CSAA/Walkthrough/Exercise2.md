---
title: "Exercise 2: Creating a Network"
---
Exercise 2: Creating a Network will take you through the process of creating a VPC, subnets, internet gateway, route table, and security group. You will also create an EC2 instance and attach it to the VPC. The EC2 instance will be configured to run Apache and PHP. The exercise was taken from [Week 2 Exercise](https://www.coursera.org/learn/aws-certified-solutions-architect-associate/home/week/2) course.

## Task 1: Creating the VPC

1. Log in to the AWS Management Console.
2. Go to the VPC Dashboard.
3. Click on "Create VPC" button.
4. Provide a name for the VPC, in this case `practice-vpc`, and provide a CIDR block, in this case ```10.0.0.0/16```.
5. Click on "Create" button.
## Task 2: Creating the internet gateway

1. From the VPC Dashboard, click on "Internet Gateways" in the left sidebar.
2. Click on "Create Internet Gateway" button.
3. Provide a name for the internet gateway, in this case `practice-igw`.
4. Click on "Create" button.
5. Select the internet gateway and click on "Actions" button.
6. Select "Attach to VPC" option.
7. Select `practice-vpc` from the list and click on "Attach" button.
## Task 3: Creating subnets

1. From the VPC Dashboard, click on "Subnets" in the left sidebar.
2. Click on "Create Subnet" button.
3. Provide a name for the subnet, in this case `Public 1` and select the VPC `practice-vpc` and the Availability Zone "AZ-a".
4. Provide a IPv4 CIDR block, in this case ```10.0.1.0/24``` .
5. Click on "Add new subnet" button.
5. Repeat steps 2-4 for the remaining three subnets, providing the names `Private 1`, `Public 2`, `Private 2`, and selecting the appropriate IPv4 CIDR block for each. For example the IPv4 CIDR blocks could be ``````10.0.2.0/24```, ```10.0.3.0/24``` and ```10.0.4.0/24``` respectively.
## Task 4: Configuring the route table

1. From the VPC Dashboard, click on "Route Tables" in the left sidebar.
2. Click on "Create Route Table" button.
3. Provide a name for the route table, in this case "practice-rtb".
4. Select the VPC `practice-vpc` and click on "Create" button.
5. Select the route table and click on "Actions" button.
6. Select "Edit Routes" option.
7. Click on "Add route" button.
8. In the "Destination" field, enter "0.0.0.0/0" and in the "Target" field, select the internet gateway "practice-igw".
9. Click on "Save" button.
10. Select the route table and click on "Actions" button.
11. Select "Associate subnet" option.
12. Select `Public 1` and `Public 2` subnets and click on "Associate" button.
## Task 5: Creating the EC2 instance and security group

1. From the EC2 Dashboard, click on "Launch Instance" button.
2. Select "Amazon Linux 2 AMI (HVM), SSD Volume Type, x86" as the AMI.
3. Select "t2.micro" as the instance type.
4. Select the VPC "practice-vpc" and the subnet "Public 1" or "Public 2"
5. Select to "Enable" auto-assign Public IP.
6. Click on "Add storage" and adjust as desired, then click on "Add Tag" and provide a name for the instance, in this case "new-instance".
7. Click on "Configure Security Group" button.
8. Click on "Create a new security group" button.
9. Provide a name for the security group, in this case `practice-sg` and add the rule "HTTP/80".
10. Scroll donw and add User Data to install Apache and PHP.
```bash
#!/bin/bash
yum update -y
amazon-linux-extras install -y lamp-mariadb10.2-php7.2 php7.2
yum install -y httpd mariadb-server
systemctl start httpd
systemctl enable httpd
usermod -a -G apache ec2-user
chown -R ec2-user:apache /var/www
chmod 2775 /var/www
find /var/www -type d -exec chmod 2775 {} \;
find /var/www -type f -exec chmod 0664 {} \;
echo "<?php phpinfo(); ?>" > /var/www/html/phpinfo.php
```
11. Click on "Review and Launch" button.