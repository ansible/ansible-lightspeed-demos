# Provision Azure resources and virtual machine

## Configure and activate Ansible Lightspeed

Install the VS Code extension and activate Ansible Lightspeed using resources in the [getting started guide](../../../getting_started.md).

### ❗️ Test suggestions using the corresponding `solution_*.yml` Playbook

The Ansible Lightspeed model continues to improve with each release and generated suggestions may differ from the examples provided.  
Tested Ansible content starts with the `solution_*.yml` prefix. For example, `solution_provision_azure_vm.yml` Please use this to compare your generated suggestions to the tested Ansible content.

## Overview

This demo provisions multiple Azure resources, such as a resource group, networking, security group, and an Azure virtual machine.  

This demo is more advanced as it has several tasks and requires manual changes to some of the suggestions. However, it's a good example of how Ansible Lightspeed uses previous task patterns, previously generated content, and variables in later suggestions.

An example Azure inventory is available in the [inventory](./inventory/) folder. It uses the [Azure Resource Manager inventory plugin](https://docs.ansible.com/ansible/latest/collections/azure/azcollection/azure_rm_inventory.html).

![](../../../assets/img/lightspeed_provision_azure_vm.gif)

## Demo preparation

1. Use environment variables to configure your Azure credentials as outlined in the [Ansible Microsoft Azure guide](https://docs.ansible.com/ansible/latest/scenario_guides/guide_azure.html#using-environment-variables).
2. Run the [./prepare_azure_environment.yml](./prepare_azure_environment.yml) Playbook to create the required Azure demo resources before running the `demo_provision_azure_vm.yml` Playbook.

### Accessing the instance

1. The `./prepare_azure_environment.yml` creates a temporary SSH private `*_ssh_key` and public `*_ssh_key.pub` key file in the `./playbooks/cloud/azure/files/` folder to access the instance.
2. An example inventory is located the [inventory folder](./inventory/).

## Running the demo

### Ansible demo content

#### Ansible Playbook to use in the demo

[./playbooks/cloud/azure/demo_provision_azure_vm.yml](./demo_provision_azure_vm.yml)

#### Tested Ansible Playbook to compare your results

[./playbooks/cloud/azure/solutions/solution_provision_azure_vm.yml](./solution_provision_azure_vm.yml)

Run the steps below in the initial [./playbooks/cloud/azure/demo_provision_azure_vm.yml](./demo_provision_azure_vm.yml) example Ansible Playbook.

### Step 1

#### Uncomment and generate the first task `- name: Create a Standard_A1_v2 RHEL 8 VM called vm-lightspeed`

- Suggestion used the Playbook name, `Create Azure VM`, to know the suggestion should use the `azure.azcollection` Content Collection.
- Used natural language prompt to generate syntactically correct Ansible Playbook task.
- Suggestion incorporated Ansible best practices and used Fully Qualified Collection Name (FQCN).
- Used `...Standard_A1_v2 RHEL 8 VM called vm-lightspeed...` in the task description to correctly fill in the module arguments.

### Step 2

#### Remove the previous task and generate a new task with  `- name: Create a VM called vm-lightspeed using vm_config var`

- Ansible Lightspeed used the updated natural language prompt and integrated the `vm_config` variable in the suggestion.

---
