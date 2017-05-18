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

CloudFront has cost-saving over serving from S3, an increase in speed, and CloudFront caches the S3 content.  Can control with a low TTL.

