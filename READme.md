# S3 Sync with GitHub Actions

This repository contains a GitHub Actions workflow for securely syncing a local directory to an AWS S3 bucket. The workflow automates the process of syncing files and deleting files in AWS S3 bucket. 

## Features
- Sync files (create/delete) to an AWS S3 bucket when code is pushed to the `main` branch.
- Use AWS roles and temporary credentials for secure access.

## Prerequisites
1. An AWS S3 bucket.
2. An IAM role with the necessary permissions:
   - `s3:ListBucket` (bucket level)
   - `s3:DeleteObject` and `s3:GetObject` (object level).
3. Secrets configured in your GitHub repository:
   - `AWS_REGION`: The AWS region of your S3 bucket.
   - `AWS_IAM_ROLE`: The ARN of the IAM role to assume.
   - `AWS_BUCKET_NAME`: The name of your S3 bucket.


## Application
- [Github Actions and AWS Security Integration Diagram](images/aws-githubactions.drawio.png)
- [IAM Policy](images/aws-iam-s3-policy.png)
- [IAM Role](images/aws-bucket-trust-role.png)
- [S3 Bucket](images/aws-s3-bucket.png)


## Resources
- [DaveOps Tutorial](https://www.youtube.com/watch?v=HEOU6o-Eazs&t=321s)
- [AWS Marketplace action](https://github.com/marketplace/actions/configure-aws-credentials-action-for-github-actions)

## Contributing
Feel free to submit issues or pull requests for improvements or bug fixes.

