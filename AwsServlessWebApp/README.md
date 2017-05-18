# AWS Servless Web App

## Tech Stack
- API Gateway
- Lambda Functions
- CLI

## Static Content
- HTML5, CSS
- Javascript
 - Bootstrap
 - VueJS
- Repo - src/ww
- Deployed to S3 (reduced-redundancy)
- Served By CloudFront

CloudFront has cost-saving over serving from S3, an increase in speed, and CloudFront caches the S3 content.  Can control with a low TTL.  Also provided NAT, Blacklisting, etc.

## API's
- NodeJS 6
- Deployed to Lambda
- Served by API Gateway
- Website: Contact Form

### Tool: Lambda Local
https://www.npmjs.com/package/lambda-local

## Build and Deploy
- COnfigure - ./configure
  * Currently: Set AWS Region
- Build both stacks - make stack
- API's
  * make text - test lambda code locally (Lambda-local)
  * make build - Package into ZIP
  * make lambda - Deploys code into Lambda
  make deploy - Deploy API Gateway endpoint
- Static Content
  * make sync



