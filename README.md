# About

<p align="center">🚧 Under Construction 🚧</p>

The unofficial documentation for AWS Certified Solutions Architect - Associate.
I am working on this website during my preparation for the exam. The goal is to have a website that contains all the information in simple and easy to understand terms. I will be adding more content as I go through the exam preparation. As I keep adding more content, I will be updating the website to make it more user friendly. Adding search functionality and improving the document’s structure.              
   

# Status:

- [x] Development stage hosted on Netlify: https://aws-notes-taking.netlify.app/
- [x] Early production stage hosted on AWS Amplify: TBA
- [ ] Custom domain name


# AWS Amplify solution

The following is the simplest architecture to support the build stages in production using AWS Amplify everything is basically managed automatically. From git push to the website deployment.

![Architecture](./static/img/website-simple-architecture.png)

# Amazon S3 + CloudFront solution

The following are the technologies to support the build stages in production.

- GitHub
- AWS CodePipeline
- AWS CodeStar
- Amazon S3
- Amazon CloudFront

![Architecture](./static/img/website-expected-architecture.png)

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
