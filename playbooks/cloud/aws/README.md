# Provision an AWS EC2 instance using Ansible Lightspeed

![](../../../assets/img/lightspeed_provision_aws_instance.gif)

## Configure and activate Ansible Lightspeed

Install the VS Code extension and activate Ansible Lightspeed using resources in the [getting started guide](../../../getting_started.md).

### ❗️ Test suggestions using the corresponding `solution_*.yml` Playbook

The Ansible Lightspeed model continues to improve with each release and generated suggestions may differ from the examples provided.  
Tested Ansible content starts with the `solution_*.yml` prefix. For example, `solution_provision_ec2_instance.yml` Please use this to compare your generated suggestions to the tested Ansible content.

## Overview

This demo provisions an AWS EC2 instance using pre-existing variables.

## Demo preparation

1. Configure your AWS credential environment variables as outlined in the [Ansible AWS guide](https://docs.ansible.com/ansible/latest/collections/amazon/aws/docsite/guide_aws.html#authentication).
2. Run the [./prepare_ec2_environment.yml](./prepare_ec2_environment.yml) Playbook to create the required AWS demo resources before running the `demo_provision_aws_instance.yml` Playbook.

### Accessing the instance

1. If you're running this outside of the [Ansible Interactive Labs (Instruqt)](https://www.redhat.com/en/interactive-labs/ansible) environment, the `./prepare_ec2_environment.yml` creates a temporary SSH private .pem key file in the `./playbooks/cloud/aws/files` folder to access the instance.
2. An example inventory is located the [inventory folder](./inventory/).

## Running the demo

### Ansible demo content

#### Initial Ansible Playbook

[./playbooks/cloud/aws/demo_provision_ec2_instance.yml](./demo_provision_ec2_instance.yml)

#### Tested Ansible Playbook

[./playbooks/cloud/aws/solution_provision_ec2_instance.yml](./solution_provision_ec2_instance.yml)

Run the steps below in the [./playbooks/cloud/aws/demo_provision_aws_instance.yml](./demo_provision_ec2_instance.yml) example Ansible Playbook.

### Step 1

#### Generate multi-task `# Gather info from subnet called subnet-lightspeed & create vpc_subnet_id var`

- Used natural language prompt to generate syntactically correct Ansible Playbook Task.
- Suggestion incorporated Ansible best practices and used Fully Qualified Collection Name (FQCN).
- The first task used the correct AWS tag "tag:Name" in the filter.
- The second task used the correct variable created in the previous task.

### Step 2

#### Uncomment and generate task `- name: Provision t3.small instance using ec2_instance var`

- Used details specified in the prompt. For example, "t3.small"
- The suggestion used the "ec2_instance" variable declared in the "vars:" section.

### Step 3

#### Generate multi-task `# Create var from public_ip_address with retry & print it out`

- The suggestion used the correct variable from the previous task and added the `retries` paramater.
- The second task used the "public_ip_address" variable based on the previous task.

---
