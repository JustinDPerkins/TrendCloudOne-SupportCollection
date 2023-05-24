# Trend Cloud One File Storage Security - CloudWatch Log Collection Tool

This tool is intended to aid in generating and collecting the File Storage Security Lambda CloudWatch logs and Stack provided parameters.
The output of this tool can be provided to Trend Micro Support on case creation.

---

### Requirements fo use.

### SSM Automation Operations IAM Role
- Create an IAM Role for SSM Automations to Assume to execute document. See example [SSM-Policy](https://github.com/JustinDPerkins/TrendCloudOne-SupportCollection/blob/main/File-Storage-Security/aws/ssm-iam-example-policy.json)
- The IAM Role requires SSM to be a Trusted Entity.

## S3 Requirements.
- File Storage Security must be deployed and monitoring a S3 bucket.



---

### What is supported?
- Same Account/Region FSS Deployments.

---

## How Can this tool be used?

### Via AWS Console:
Systems Manager > Documents > All Documents > "Trend-FileStorageSecurity-SupportCollectionTool"
- Provide the ARN value of the IAM Role SSM will assume.(SSM Trusted Entity)
- Provide the Scanner Stack Name.
- Provide the Storage Stack Name.
- Provide the Name of an S3 bucket to upload package to.

### Via AWS CLI:
- Linux CLI:
```
aws ssm start-automation-execution --document-name "Trend-FileStorageSecurity-SupportCollectionTool" --document-version "\$DEFAULT" --parameters '{"AutomationAssumeRole":["<SSM IAM Automation Role ARN Here>"],"ScannerStackName":["<Scanner-Stack-Name-Here>"],"StorageStackName":["<Storage-Stack-Name-Here>"],"ArtifactBucket":["<Bucket-4-Artifacts-Name-Here>"]}' --region us-east-1
```


