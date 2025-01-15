EBS Volume Cleanup Script
Overview
This repository contains a Python script that helps identify and clean up unused Amazon Elastic Block Store (EBS) volumes in an AWS environment. Forgotten EBS volumes can incur unnecessary costs, and this script automates the process of detecting and optionally deleting such volumes.

How It Works
The script performs the following steps:

Identifies Unused Volumes:
It uses the AWS SDK for Python (boto3) to list all EBS volumes with the status available (not attached to any EC2 instance).

Deletes Unused Volumes:
It attempts to delete these volumes. If a deletion fails (e.g., due to permissions), it logs the error.

Logs Actions:
All deleted volumes are logged in the output, along with any errors encountered.

Pre-requisites
AWS Account
You need an active AWS account with appropriate permissions to list and delete EBS volumes.

AWS Credentials
Ensure your AWS credentials are configured. You can do this via:

AWS CLI (aws configure)
Environment variables
IAM role (if running on an AWS instance or Lambda function)
Python Environment
Install Python 3.7+ and the boto3 library:

bash
pip install boto3
