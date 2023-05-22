# Trend Cloud One File Storage Security - CloudWatch Log Collection Tool

This tool is intended to aid in generating and collecting the File Storage Security lambda cloudwatch logs.

---

### Requirements fo use.
- File Storage Security deployed on AWS.
- SSM Automation IAM Role.

---

### SSM Automation IAM role
- Create an IAM Role for SSM Automations to Assume. See example [SSM-Policy](https://github.com/JustinDPerkins/TrendCloudOne-SupportCollection/blob/main/File-Storage-Security/aws/ssm-iam-example-policy.json)

---

### What is supported?
- Same Account/Region Deployments

---

### How to run?
- Provide the ARN value of the IAM Role SSM will assume.(SSM Trusted Entity)
- Proved the Scanner Stack Name.
- Provide the Storage Stack Name.
- Provide the Name of an S3 bucket to upload package to.(EC2 will need permissions to this bucket to put objects)
