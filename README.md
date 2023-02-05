# About

Welcome to the AWS Certified Solutions Architect - Associate Handbook! This comprehensive resource serves as your go-to guide for all things related to the AWS Certified Solutions Architect - Associate certification. The site features an appendix detailing the various AWS services, as well as a convenient search function to help you quickly find the information you need. Whether you're a seasoned professional or just starting your journey with AWS, this handbook is a valuable tool that will help you prepare for the certification exam and gain a deeper understanding of the AWS platform. So, dive in and start exploring!           


# Status:

- [x] Development stage hosted on Netlify
- [x] Production stage hosted on AWS
- [x] Custom domain name

# AWS hosting solutions

Reviewing AWS hosting solutions, these are the essential services to host a website on AWS. Some of the services are not mentioned e.g. AWS Route 53, VPC, and IAM... We cover these services in the handbook in more detail.


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
