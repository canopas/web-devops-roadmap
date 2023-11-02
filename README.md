<h1 align="center">Web DevOps Roadmap</h1>

<p align="center">
    <img src="https://github.com/canopas/web-devops-roadmap/blob/main/images/title_image.png">
</p>

This repository contains a basic DevOps roadmap for all web developers. Anyone can start this training with their existing learning projects. The approximate duration to complete this roadmap is 10 days, it can vary based on experience though.

# Guidelines
- Before starting any practice, it's essential to conduct research and learn the necessary concepts.

- Create a GitHub/GitLab repository for each Practical if one doesn't already exist.

- Learn Basic DevOps Principles:
  - How to use Version Control effectively for your codebase as Git is Fundamental.
  - How to write unit tests.
  - Understand the core DevOps concepts like continuous integration, continuous deployment, and automation.
  - Basic scripts to get an overall understanding of scripting language.
  - Basic security practices like exposing env vars, Inbound/Outbound security rules, etc…

- Note for Cloud platforms like AWS/Gcloud/Azure:
  - Start deploying an application manually through the AWS/Gcloud/Azure console. It will provide a solid foundational understanding of the service.
  - Once you've gained proficiency in this approach, transitioning to CI/CD becomes a easy process.

- Some Basic Guidelines for CI/CD:
  - Understand the CI/CD concepts and their significance with pipeline usage.
  - Learn how to set up the basic CI/CD pipeline with the GitLab/GitHub-CI tool.
  - All lint rules should be passed from the pipeline.
  - Always use the latest versions of languages and project dependencies
  - Understand how to manage project dependencies using NPM(Node Package Manager), Yarn, Composer, or Vendors. And integrate them into the pipeline.
  - Learn to automate the testing into the CI/CD pipeline.
  - Learn how to use environment variables effectively in CI/CD pipelines including handling sensitive information like secret keys or passwords.

---

# Prerequisites

Learn following before starting practice.

- Linux commands for DevOps
    - Install dependencies
    - File operations
    - SSH commands
- [Docker](https://docs.docker.com/get-started/overview/)
    - Concepts
      - swarm
      - services
      - images
      - containers
      - tags
      - volume
      - docker-compose
    -  Create image
    -  Create container
    -  Run container locally
    -  Push on the registry
    -  Remove unused services or data
- [Version control system](https://learn.microsoft.com/en-us/devops/develop/git/what-is-version-control) and [git](https://www.nobledesktop.com/learn/git/what-is-git)
- [What is cloud computing?](https://aws.amazon.com/what-is-cloud-computing/)
- [AWS account](https://aws.amazon.com/console/)

---

# Table of contents

- [Practical 1 - Linting javascript code with eslint](https://github.com/canopas/web-devops-roadmap#practical-1---linting-javascript-code-with-eslint)

- [Practical 2 - Linting PHP code and add pre-commit hook](https://github.com/canopas/web-devops-roadmap#practical-2-linting-php-code-and-addpre-commit-hook)

- [Practical 3 - Linting Golang code](https://github.com/canopas/web-devops-roadmap#practical-3---linting-golang-code)

- [Practical 4 - Unit test check in golang](https://github.com/canopas/web-devops-roadmap#practical-4---unit-test-check-in-golang)

- [Practical 5 - Build a Docker image](https://github.com/canopas/web-devops-roadmap#practical-5---build-a-docker-image)

- [Practical 6 - AWS EC2 Deployment](https://github.com/canopas/web-devops-roadmap#practical-6---aws-ec2-deployment)

- [Practical 7 - Configure Proxy and DNS Hosting](https://github.com/canopas/web-devops-roadmap#practical-7---configure-proxy-and-dns-hosting)

- [Practical 8 - Deploy Nuxt static website on AWS S3 with Cloudfront](https://github.com/canopas/web-devops-roadmap#practical-8---deploy-nuxt-static-website-on-aws-s3-with-cloudfront)

- [Practical 9 - Deploy golang API on AWS Lambda with Route53 hosting using CloudFormation stack](https://github.com/canopas/web-devops-roadmap#practical-9---deploy-golang-api-on-aws-lambda-with-route53-hosting-using-cloudformation-stack)

---

# Ensure code quality

### Practical 1 - Linting javascript code with eslint

**Expected -** Configure GitLab workflow for Linting and Formatting, that should be passed without errors.

- Set up the Vue.js project with typescript and create the simple component with tailwind css.
  
- Integrate eslint and perform following rules,
  - Enforce naming conventions for files and folder names
  - Enforce naming conventions for variables and function names
  - Use semicolons at the end of statements
  - Use double quotes for strings
  - Enforce no trailing spaces, consistent line endings (e.g., LF or CRLF), and consistent spacing around operators
  - Limit the line length to a maximum of 100 characters
  - Limit the max 300 lines for files
  - Limit the max 30 lines for functions
  - Enforce 2 space identation
  - Ignore eslint check in non-javascript files
  
- Write GitLab CI script to run lint
  - Create a repository on GitLab if one doesn't already exist
  - Configure the script to run ESlint as part of the CI/CD pipeline.
  - Ensure that the linting process runs on each commit.

### Practical 2 - Linting PHP code and add pre-commit hook

**Expected -** Configure GitLab workflow for Linting and Formatting, that should be passed without errors.

- Set up a PHP e-commerce project and learn PHP linters.

- Perform following rules,
  - Enforce naming conventions for files and folder names
  - Enforce naming conventions for variables and function names
  - Use semicolons at the end of statements
  - Use double quotes for strings
  - Enforce no trailing spaces, consistent line endings (e.g., LF or CRLF), and consistent spacing around operators
  - Limit the line length to a maximum of 100 characters
  - Limit the max 300 lines for files
  - Limit the max 30 lines for functions
  - Enforce 2 space identation
  - Setup prettier and format code with prettier
  - Ignore checks in non-php files

- Write GitLab CI script to run lint
  - Create a repository on GitLab if one doesn't already exist
  - Configure the Pre-commit hook to run prettier before the commit
  - Configure the script to run Lint as part of the CI/CD pipeline.
  - Ensure that the linting process runs on each commit.

### Practical 3 - Linting Golang code

**Expected -** Configure GitHub workflow for Linting and Formatting, that should be passed without errors.

- Set up Golang API project and learn Golang linters.
  
- Perform following rules,
  - Enforce naming conventions for files and folder names
  - Enforce naming conventions for variables and function names
  - Limit the line length to a maximum of 100 characters
  - Limit the max 300 lines for files
  - Limit the max 30 lines for functions
  - Format code
  - Ignore check in non-go files
  
- Write GitHub CI script to run lint
  - Create a repository on GitHub if one doesn't already exist
  - Configure the Pre-commit hook to run prettier before the commit
  - Configure the script to run Lint as part of the CI/CD pipeline.
  - Ensure that the linting process runs on each commit.

---

# Automate Testing

### Practical 4 - Unit test check in golang

**Expected -** Configure GitHub workflow for Linting and Formatting, that should be passed without errors.

- Write unit tests from [Practical 22](https://github.com/canopas/web-developer-roadmap-2023#practical-22) if not already written.

- Ensure the test covers all the success and error cases and passes with 85% code coverage.

- Write GitHub CI script to run Unit test
  - Create a repository on GitHub if one doesn't already exist
  - Configure the database and script to run unit tests as part of the CI/CD pipeline.
  - Ensure that the unit test runs on each commit.

---

# Deployment

## Running project using Docker on AWS EC2

### Practical 5 - Build a Docker image

**Expected -** Docker image should be available on GitLab Registry.

- Set up [VueJs- admin panel](https://github.com/canopas/web-developer-roadmap-2023#practical-18) project if one doesn't already exist

- Write GitLab CI script to run docker build
  - Create a repository on GitLab if one doesn't already exist
  - Write a docker file which includes,
    - Install dependencies
    - Build and run project
  - 
  - Write a CI/CD script for Building a docker image and push it on the GitLab Registry.

### Practical 6 - AWS EC2 Deployment

**Expected -** Admin panel successfully run on `<ec2-ip-address>:<docker-container-port>`.

- Perform following steps on AWS console
  - Create EC2 instance with Security rules
  - Install docker and enable docker swarm on the EC2 instance

- Create a docker-compose file for the above docker image

- Write GitLab CI script to deploy docker image on EC2 instance using docker-compose

### Practical 7 - Configure Proxy and DNS Hosting

**Expected -** Admin panel should run on DNS(i.e - admin.example.com).

- Configure NGINX for [VueJs- admin panel](https://github.com/canopas/web-developer-roadmap-2023#practical-18).
  - Create Self-signed SSL certificates for testing using OpenSSL and configure them in NGINX
  - Write a rule to allow http to https redirection
  - Add reverse proxy for your project with DNS

- Add NGINX configuration in Docker-compose which performs,
  - Copy certificates to etc/nginx/certs on EC2
  - Copy config files to etc/nginx/conf.d on EC2

- Write CI/CD script for running nginx container on EC2 instance

- Cloudflare configuration
  - Create Cloudflare account if not already created 
  - Add DNS(i.e - admin.example.com) on Cloudflare and proxy it to NGINX

## Static site deployment

### Practical 8 - Deploy Nuxt static website on AWS S3 with Cloudfront

**Expected -** The Website should run on the Cloudfront domain name.

- Set up a nuxt-project if one doesn't already exist
- Create SPA using a Static-site generator in Nuxt

- Create S3 Bucket and Cloudfront distribution on the AWS console
- Point Bucket link to Cloudfront origin

- Write GitHub CI/CD to Generate a static website and deploy it on AWS S3

## API deployment on AWS Lambda and API Gateway

### Practical 9 - Deploy golang API on AWS Lambda with Route53 hosting using CloudFormation stack

**Expected -** API should be accessible from Route53 DNS
- Set up Golang API project using Gin if one doesn't already exist. ([Practical 22](https://github.com/canopas/web-developer-roadmap-2023#practical-22))
- Use AWS SDK and Prepare code for Golang to deploy it to Lambda

- Write GitHub CI/CD script for deploying cloudformation stack which includes,
  - Define IAM's role and policies to provide required access
  - Create AWS Lambda function for Golang
  - Create an API Gateway that can access the above Lambda function
  - Create Custom domain and API mapping
  - Configure Route53 DNS for API Gateway proxy
