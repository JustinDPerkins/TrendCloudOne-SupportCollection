# Trend Cloud One Workload Security - Agent Diagnostic Collection Tool

This tool is intended to aid in generating and collecting the workload security agent diagnostic log package.

---

### Requirements fo use.
- Workload Security Agent deployed on instance.
- Instance must have SSM Managed IAM Role and S3 to upload log package.
- SSM Automation IAM Role.

---

### SSM Automation IAM role
- Create an IAM Role for SSM Automations to Assume.

---

### What is supported?
- Linux OS
- Windows OS

---

### How to run?
- Provide the ARN value of the IAM Role SSM will assume.(SSM Trusted Entity)
- Proved the Instance ID. (i-1234567890)
- Provide the Name of an S3 bucket to upload package to.(EC2 will need permissions to this bucket to put objects)
