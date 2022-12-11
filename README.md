# About

<p align="center">🚧 Under Construction 🚧</p>

The unofficial documentation for AWS Certified Solutions Architect - Associate.
I am working on this website during my prepartion for the exam.

# Amazon CloudFront solution

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
