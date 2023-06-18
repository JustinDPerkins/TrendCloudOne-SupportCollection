# Trend Cloud One Network Security - VPC Configuration Collection Tool

This tool is intended to aid in generating and collecting the VPC configuration for Network Security Deployments.
The output of this tool can be provided to Trend Micro Support on case creation.

---

## Requirements for use.

### SSM Automation Operations IAM Role
- Create an IAM Role for SSM Automations to Assume to execute document. See example [SSM-Policy](https://github.com/JustinDPerkins/TrendCloudOne-SupportCollection/blob/main/Network-Security/aws/ssm-iam-example-policy.json)
- The IAM Role requires SSM to be a Trusted Entity.
- The IAM Role will need S3:PutObject permissions to upload vpc configuration package to S3.

---

### Limitations:
- Same Account/Region

---
## How Can this tool be used?

### Via AWS Console?
Systems Manager > Documents > All Documents > "Trend-NetworkSecurity-SupportCollectionTool"
- Provide the ARN value of the SSM Automation Operation IAM Role will assume.(SSM Trusted Entity)
- Provide a singular VPC-ID value.
- Provide the Name of the S3 bucket to upload the package to.




