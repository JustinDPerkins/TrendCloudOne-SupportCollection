# Trend Cloud One Workload Security - Agent Diagnostic Collection Tool

This tool is intended to aid in generating and collecting the workload security agent diagnostic log package.

---

## Requirements for use.
- SSM Automation IAM Role.

### SSM Automation Operations IAM Role
- Create an IAM Role for SSM Automations to Assume to execute document. See example [SSM-Policy](https://github.com/JustinDPerkins/TrendCloudOne-SupportCollection/blob/main/Workload-Security/aws/ssm-iam-example-policy.json)
- The IAM Role requires SSM to be a Trusted Entity.

### Instance Requirements:
- Requires Workload Security Agent to be deployed on instance.
- Requires SSM Agent to be Installed and Running. See [here](https://docs.aws.amazon.com/systems-manager/latest/userguide/ssm-agent.html)
- The EC2 Instance requires an IAM Role with SSMManagedCore permissions.
- The EC2 will need an IAM Role with S3:PutObject permissions to upload diagnostic package to S3.
- The Instance will require the AWS CLI to be installed. See [here](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)


---

### What is supported?
- Linux OS
- Windows OS

---

### How to run?
- Provide the ARN value of the SSM Automation Operation IAM Role will assume.(SSM Trusted Entity)
- Proved an Instance ID. (i-1234567890)
- Provide the Name of the S3 bucket to upload the diagnostic package to.(EC2 will need permissions to this bucket to put objects)
