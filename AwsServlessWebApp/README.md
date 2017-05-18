# AWS Servless Web App
Darrin Lichty
Panalogy

## Source Code
https://github.com/Panology/aws-serverless-website-workshop


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


Using Cloud Formation, the deployment process is:
1. ZIp the lambda
2. Run stack that creates the bucket
3. Upload zipfile to s3 Bucket - this is versioned, so the prior version is accessible and easy to rollback

The "make sync" step uses a config.json that has the API endpoint hard-coded.  A better way might be to use a CNAME on the API GAteway.

Gluing Cloud Fron to S3 uses OAI - Object Access Identity.  They needed a custom resource
OAI: {
      Type: "Custom::CloudFrontIdentity",
        "Properties: {ServiceToken ...}
},
"staticContentPolicy: : "Type: Aws::S3::BucketPolicy"...

PriceClass_100 this priceclass is lessexpensive and only serves North Ameruca



