<h1 align="center">CloudGuardAudit 🔐</h1>
<p align="center">
  <strong>Secure your AWS cloud in minutes — audit, detect, and harden misconfigurations with Terraform.</strong>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/python-3.8%2B-blue?logo=python&logoColor=yellow" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="MIT License">
  <a href="https://github.com/MaheshShukla1/CloudGuardAudit/actions/workflows/terraform.yml" target="_blank">
  <img src="https://github.com/MaheshShukla1/CloudGuardAudit/actions/workflows/terraform.yml/badge.svg" alt="Terraform Validation">
</a>

  <img src="https://img.shields.io/github/stars/MaheshShukla1/CloudGuardAudit?style=social" alt="GitHub stars">
</p>

---
## 🚀 Overview

**CloudGuardAudit** is a developer-friendly **AWS Security Audit CLI tool** with built-in **Terraform modules** for automating secure cloud infrastructure.

It allows you to:

- 🔍 **Scan AWS resources** for vulnerabilities: public S3 buckets, open security groups, risky IAM policies, CloudTrail & GuardDuty misconfigs.
- ⚙️ **Generate automated security reports** in JSON and HTML formats.
- 🛡️ **Deploy secure AWS infrastructure** using Terraform modules following best practices.
- 🐳 Use via **CLI or Docker**, supporting AWS profiles and region-based targeting.

Whether you're a cloud engineer, DevOps, security analyst, or SRE — this tool gives you **quick visibility** into security gaps and the tools to **close them fast**.

---

## 📋 Table of Contents

- [Features](#features)  
- [Demo](#demo)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Terraform Automation](#terraform-automation)  
- [Project Structure](#project-structure)  
- [Contributing](#contributing)  
- [FAQ](#faq)  
- [License](#license)  
- [Contact](#contact)  
- [Acknowledgements](#acknowledgements)  
---

## Features

- ✅ Detect public S3 buckets exposing sensitive data  
- ✅ Identify open Security Groups (0.0.0.0/0 ingress)  
- ✅ Audit IAM users and attached policies  
- ✅ Check for multi-region CloudTrail enablement  
- ✅ Validate presence of GuardDuty detectors  
- ✅ Auto-generate detailed HTML + JSON reports  
- ✅ CLI flags for custom checks, AWS profiles & region targeting  
- ✅ Docker container support for zero setup  
- ✅ Terraform modules to deploy secured infra:  
  - 🔒 S3 buckets with access restrictions  
  - 🎯 GuardDuty setup  
  - 🧾 CloudTrail logging  
  - 🔐 Hardened Security Groups  
- ✅ GitHub Actions support  
- ✅ Unit-tested and actively maintained

---

## Demo

_Visual output of the CLI audit and HTML report preview goes here._

> You can embed a `demo.gif` or link to a YouTube walkthrough here later.

---

## Prerequisites

- ✅ Python 3.8+  
- ✅ AWS CLI configured with credentials  
- ✅ Terraform v1.0+ (for IaC automation)  
- ✅ Docker (optional but recommended)

---

## Installation

### Clone the repository

```bash
git clone https://github.com/yourusername/cloudguardaudit.git
cd cloudguardaudit
```

### Setup Python environment and install dependencies

```bash
python3 -m venv venv source venv/bin/activate
# Windows: venv\Scripts\activate pip install -r requirements.txt`
```
---

## Usage

### ✅ Run all audit checks against your AWS account

```bash
`python -m cloudsentinel.cli --check all --region us-east-1 --profile default`
```
---

### ✅ Generate an example config file for customization

```bash
`python -m cloudsentinel.cli --generate-config`
```
---

### ✅ Use a custom config file and run selective checks

```bash
`python -m cloudsentinel.cli --config example-config.yaml --check s3,sg`
```
---

### ✅ Run audit inside Docker container (no setup required)

```bash
`docker build -t cloudguardaudit . docker run --rm -e AWS_PROFILE=default cloudguardaudit --check all --region us-east-1`
```
---

## Terraform Automation
Deploy secure AWS infrastructure using the built-in Terraform modules:

```bash
`cd terraform terraform init terraform apply -var-file=../terraform.tfvars`
```

> ⚠️ **Note:** Customize the `terraform.tfvars` file with your AWS environment-specific values before applying.

---

## Project Structure

```plaintext
cloudguardaudit/
├── cloudsentinel/            # Python CLI audit tool source code
├── terraform/                # Terraform modules & infrastructure code
├── tests/                    # Unit and integration tests
├── scripts/                  # Helper scripts & utilities
├── example-config.yaml       # Sample audit tool YAML config
├── requirements.txt          # Python dependencies
├── Dockerfile                # Docker container definition
├── README.md                 # This documentation file
├── LICENSE                   # Project license (MIT)
└── terraform.tfvars          # Terraform variables (excluded from VCS)
```
---

## Contributing

We welcome contributions from the community!

- ✅ Submit issues for bugs or ideas
    
- ✅ Open pull requests with new audit checks or improvements
    
- ✅ Improve Terraform modules
    
- ✅ Enhance documentation
    

Please read `CONTRIBUTING.md` before submitting your first PR.

---

## FAQ

**Q: What AWS permissions are required to run the audit?**  
A: The tool requires read access to S3, EC2, IAM, CloudTrail, and GuardDuty APIs.

**Q: How do I provide credentials?**  
A: Configure your AWS CLI or pass `--profile` with a named profile.

**Q: Does this tool fix the security issues?**  
A: No, it only reports risks. Use the provided Terraform modules to deploy secure infrastructure.

**Q: Is it production-safe?**  
A: Yes, the audit is read-only. Terraform modules should be reviewed before applying.

---

## License

This project is licensed under the **MIT License**.  
See the LICENSE file for full details.

---

## Contact

Made with ❤️ by Your Name  
Follow me on LinkedIn for updates and new projects.

---

## Acknowledgements

Inspired by AWS security best practices, DevSecOps workflows, and contributions from the open-source community.
