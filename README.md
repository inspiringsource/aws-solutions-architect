# AWS Handbook for SAA-C03 Certification

## About
Welcome to the AWS Handbook for SAA-C03 certification, an open-source guide to aid you in preparing for the AWS Certified Solutions Architect - Associate exam. This handbook provides detailed information on AWS services. While some content is generated using GitHub Copilot, everything has been thoroughly reviewed. I no longer host the website, but you can clone the repository and run it locally.

## Status

- ~~[x] Development stage hosted on Netlify~~
- ~~[x] Production stage hosted on AWS~~
- ~~[x] Custom domain name~~

## AWS Hosting Solutions
This section provides insights into essential AWS services for hosting solutions focused on frontend client-side rendering. Detailed service descriptions and architectural diagrams are included. Note: AWS Route 53, VPC, and IAM are not covered in depth here as they indirectly relate to hosting but are essential for domain management, network creation, and user permissions management.

### AWS Amplify
AWS Amplify offers a complete backend and frontend cloud development platform that is ideal for building scalable, secure web applications that perform client-side rendering. It integrates CloudFront to globally distribute content, enhancing performance and securing applications against DDoS attacks.

![AWS Amplify Architecture Diagram](./static/img/website-simple-architecture.png)

### Amazon S3 + CloudFront
Host a static website using Amazon S3 along with CloudFront, supporting technologies such as GitHub, AWS CodeStar, and AWS CodePipeline. This setup is particularly effective for websites that utilize client-side rendering.

![S3 + CloudFront Architecture Diagram](./static/img/website-expected-architecture.png)

### EC2 Deployment
Deploy a React.js application that performs client-side rendering on EC2. This approach is supported by AWS services including AWS CodePipeline, AWS CodeBuild, and AWS CodeDeploy.

![EC2 Hosting Architecture Diagram](./static/img/hosting-ec2-architecture.png)

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
