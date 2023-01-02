# About

<p align="center">🚧 Under Construction 🚧</p>

The unofficial documentation for AWS Certified Solutions Architect - Associate.
I am working on this website during my preparation for the exam. The goal is to have a website that contains all the information in simple and easy to understand terms. I will be adding more content as I go through the exam preparation. As I keep adding more content, I will be updating the website to make it more user friendly. Adding search functionality and improving the document’s structure.              
   

# Status:

- [x] Development stage hosted on Netlify: https://aws-notes-taking.netlify.app/
- [x] Production stage hosted on AWS: TBA
- [ ] Custom domain name

# AWS hosting solutions

Reviewing AWS hosting solutions for hosting the website. The following are the technologies that can be used to support this build:
## AWS Amplify solution

AWS Amplify provides a complete backend and frontend cloud development platform with powerful tools for app development, including continuous integration and delivery.

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
