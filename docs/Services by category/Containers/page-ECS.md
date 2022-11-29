---
title: Amazon ECS
description: Lorem ipsum dolor sit amet - 2

---

Amazon Elastic Container Service (Amazon ECS) is a highly scalable, fast, container management service that makes it easy to run, stop, and manage Docker containers on a cluster. Your containers are defined in a task definition that you use to run individual tasks or tasks within a service.

## Amazon ECS task definitions

Your Amazon ECS tasks can have an IAM role associated with them. The permissions granted in the IAM role are assumed by the containers running in the task. [IAM roles for tasks](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html)

A task definition is required to run Docker containers in Amazon ECS. The following are some further parameters that you can specify in a task definition:

- The Docker image to use with each container in your task

- How much CPU and memory to use with each task

- The launch type to use, which determines the infrastructure that your tasks are hosted on

- The operating system of the container that the task run on

- The Docker networking mode to use for the containers in your task

- The logging configuration to use for your tasks

- Whether the task continues to run if the container finishes or fails

- The command that the container runs when it's started

- Any data volumes that are used with the containers in the task

[Source](https://docs.aws.amazon.com/AmazonECS/latest/userguide/task_definitions.html)