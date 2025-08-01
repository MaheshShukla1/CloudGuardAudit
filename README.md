# AWS Security Audit Tool 🔒

A comprehensive **AWS Security Audit Tool** built in Python using **boto3** to automate security checks on your AWS infrastructure.  
This tool helps identify critical security risks like **public S3 buckets**, **open security groups**, **IAM users with excessive permissions**, and checks for **CloudTrail** & **GuardDuty** status.  

---

## 🚀 Features

- Detects publicly accessible S3 buckets  
- Identifies open Security Groups allowing unrestricted inbound access  
- Lists IAM users and their attached policies  
- Checks if CloudTrail is enabled across regions  
- Verifies if AWS GuardDuty is active for threat detection  
- Generates a detailed JSON security audit report with timestamp

---

## 💡 Why Use This Tool?

- Ensure your AWS environment adheres to **best security practices**  
- Automate manual and error-prone security audits  
- Quickly identify **security loopholes** before they are exploited  
- Build confidence for **audits, compliance, and security reviews**  
- Ideal for **cloud engineers, security professionals, and freelancers**

---

## 📋 Requirements

- Python 3.8 or above  
- AWS CLI configured with appropriate permissions (`aws configure`)  
- Python libraries: boto3 (install via `pip install -r requirements.txt`)

---

## ⚙️ Installation

```bash
git clone https://github.com/YourUsername/aws_security_audit_tool.git
cd aws_security_audit_tool
pip install -r requirements.txt
