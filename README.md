# AWS EC2 Lifecycle Automation with Ansible

This project demonstrates automation of AWS EC2 instances using Ansible. It includes playbooks to **create, manage, and terminate EC2 instances**, showcasing Infrastructure as Code (IaC) practices.

## Features

- **Provision EC2 Instances**: Launch new instances in different AWS regions.
- **Stop / Terminate Instances**: Cleanly stop or delete instances when not needed.
- **Secure Management**: Uses SSH key-based authentication and Ansible Vault for sensitive data.
- **Reusable Playbooks**: Configurable inventory and variables for multiple environments.

## Technologies Used

- Ansible
- AWS EC2
- Python (boto3)
- SSH for secure connections

## Usage

1. Configure your `inventory.ini` and `group_vars` with AWS credentials and region info.
2. Run the playbook to create instances:
   ```bash
   ansible-playbook -i inventory.ini ec2_create.yaml
   ansible-playbook -i inventory.ini ec2_stop.yaml

