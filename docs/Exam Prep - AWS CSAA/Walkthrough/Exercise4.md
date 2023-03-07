---
title: "Exercise 4: Implementing Elasticity"
---
Exercise 4: Create an Application Load Balancer in a specified VPC and region, a launch template for t3.micro instances, an Auto Scaling group attached to the load balancer, stress the CPU to trigger the scaling action, and verify the scaling by viewing the instances in the Auto Scaling group.

## Task 1: Creating the load balancer
- Create an Application Load Balancer in the specified VPC: ```Lab VPC``` and region using the subnets ```LabPublicSubnet1``` and ```LabPublicSubnet2```.
- Use the security group LabSecurityGroup for the load balancer.
- Create a listener for ```HTTP/80``` and forward to the target group created before starting this lab.

## Task 2: Creating the launch template
- Create a launch template for ```t3.micro``` instances using Amazon Linux 2 AMI.
- Use the specified region for the launch template.
- Do not include a key pair for the instances.
- Use the security group ```LabSecurityGroup``` for the instances.
- Include the (below included) user data script to install and run the Flask application.

```bash
#!/bin/bash -ex
   wget https://us-west-2-aws-training.s3.amazonaws.com/courses/SPL-TF-200-ARACL4/v1.0.0.prod-659d5815/scripts/FlaskApp.zip
   unzip FlaskApp.zip
   yum -y install python3 mysql
   pip3 install -r requirements.txt
   amazon-linux-extras install epel
   yum -y install stress
   export PHOTOS_BUCKET=${SUB_PHOTOS_BUCKET}
   export AWS_DEFAULT_REGION=us-east-1
   export DYNAMO_MODE=on
   FLASK_APP=application.py /usr/local/bin/flask run --host=0.0.0.0 --port=80
```

## Task 3: Creating the Auto Scaling group
- Create an Auto Scaling group using the launch template created in Task 2.
- Use the specified VPC and subnets for the Auto Scaling group.
- Attach the Auto Scaling group to the load balancer created in Task 1.
- Set desired instances to ```1```, minimum to ```1```, and maximum to ```2```.
- Use a target tracking scaling policy with the metric type of average CPU utilization and a target value of ```80```.

## Task 4: Simulating stress and scaling the application
- Visit the public DNS name of the application and append "/info" to the URL to test the application.
- Stress the CPU for 10 minutes to trigger the Auto Scaling group to scale.

Example: ```http://ec2-192-0-2-0.us-east-2.compute.amazonaws.com/info```

## Task 5: Verifying the scaling action
- Verify the scaling action by viewing the instances in the Auto Scaling group.