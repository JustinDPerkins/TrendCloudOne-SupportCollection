# Trend Cloud One Workload Security - Agent Diagnostic Collection Tool

This tool is intended to aid in generating and collecting the workload security agent diagnostic log package.

---

### Requirements fo use.
- Workload Security Agent deployed on instance.
- Instance must have SSM Managed IAM Role and S3 to upload log package.
- SSM Automation IAM Role.

#### About the Instance
- Requires SSM Agent to be Installed and Running. See [here](https://docs.aws.amazon.com/systems-manager/latest/userguide/ssm-agent.html)
- The EC2 Instance requires an IAM Role with SSMManagedCore permissions.
- The EC2 will need an IAM Role with S3:PutObject permissions to upload diagnostic package to S3.
- The Instance will require the AWS CLI to be installed. See [here](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

---

### SSM Automation IAM role
- Create an IAM Role for SSM Automations to Assume. See example [SSM-Policy](https://github.com/JustinDPerkins/TrendCloudOne-SupportCollection/blob/main/Workload-Security/aws/ssm-iam-example-policy.json)

---

### What is supported?
- Linux OS
- Windows OS

---

### How to run?
- Provide the ARN value of the IAM Role SSM will assume.(SSM Trusted Entity)
- Proved the Instance ID. (i-1234567890)
- Provide the Name of an S3 bucket to upload package to.(EC2 will need permissions to this bucket to put objects)
