# About

Welcome to the open-source AWS Handbook for SAA-C03 certification preparation. This handbook provides a comprehensive understanding of AWS with a service appendix and a convenient search function. Some of the content has been generated using GitHub Copilot, but all information has been reviewed to ensure its accuracy and ease of understanding. I hope this handbook will help you to prepare for the AWS Certified Solutions Architect - Associate exam. If you find any errors or have any suggestions, please feel free to open an issue or pull request. Also, if you find this handbook useful, please consider giving it a star ⭐️ and join the Discussions to share your thoughts and ideas.

# Status:

- [x] Development stage hosted on Netlify
- [x] Production stage hosted on AWS
- [x] Custom domain name

# AWS hosting solutions

Reviewing AWS hosting solutions, these are the essential services to host a website on AWS. Below are descriptions of the services and the architecture diagram for each solution.

> I don't cover AWS Route 53, VPC, and IAM... because they are not directly related to hosting solutions. However, you can use Route 53 to manage your domain name and VPC to create a private network for your website. You can also use IAM to manage your users and their permissions.


## AWS Amplify solution

AWS Amplify provides a complete backend and frontend cloud development platform with powerful tools for app development, including continuous integration and delivery. With Amplify, you can easily create and manage a scalable, secure and high-performing web application. Additionally, Amplify uses CloudFront by default to distribute your content globally and improve the performance of your application. With CloudFront, you can also protect your application against DDoS attacks and reduce the load on your server. This setup eliminates the need to manually configure CloudFront, hence the below architecture diagram does not include CloudFront.

![Architecture](./static/img/website-simple-architecture.png)


## Amazon S3 + CloudFront

Using Amazon S3 and CloudFront to host a static website. The following are the technologies that can be used to support this build:

- GitHub
- AWS CodeStar
- AWS CodePipeline
- AWS S3
- Amazon CloudFront


![Architecture](./static/img/website-expected-architecture.png)

## EC2 solution

Deploying the React.js app on EC2. The following are the technologies that can be used to support this build:

- GitHub
- AWS CodePipeline
- AWS CodeBuild
- Amazon S3
- AWS CodeDeploy
- Amazon EC2
- Amazon CloudFront


![Architecture](./static/img/hosting-ec2-architecture.png)

For application hosting you can also choose to use AWS Elastic Beanstalk, AWS OpsWorks, or AWS Elastic Container Service (ECS). For more information, see [AWS Application Hosting](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/application-hosting.html).
### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
