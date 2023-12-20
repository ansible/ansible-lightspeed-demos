# Ansible Lightspeed demo content

Compilation of Ansible Lightspeed demo content and examples.

## How do I get started with Ansible Lightspeed?

Please follow the instructions provided by the resources available in the [getting started guide](./docs/getting_started.md).

## Ansible Lightspeed demo list

Please refer to the `README.md` for each demo in the corresponding demo root folder for detailed demo instructions.

| **Domain**         | **Name**                                                                                                                    | **Status**  |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------|-------------|
| **Infrastructure** | [Install and configure postgresql and pgadmin4 podman container](./playbooks/infra/install_pgsql_and_pgadmin/README.md)     | Working     |
|                    | [Install and configure Cockpit](./playbooks/infra/install_cockpit/README.md)                                                | Working     |
| **Cloud**          | [Provision an AWS EC2 instance](./playbooks/cloud/aws/README.md)                                                            | Working     |
|                    | [Provision Azure resources and VM](./playbooks/cloud/azure/README.md)                                                       | Working     |

## Demo content folder structure

The repository folder structure is as follows.

```bash
.
└── playbooks/
    └── <domain>/
        └── <demo_name>/
            ├── demo_<playbook_name>.yml <-- Initial Ansible content for demo.
            ├── solution_<playbook_name>.yml <-- Tested Ansible content for comparison.
            └── prepare_<playbook_name>.yml <-- Initial Playbook to configure the demo environment.
```

| **Name**                       | **Description**                                                                                                                                                                                                        | **Example**                                                          |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| `<domain>`                     | Ansible examples are sorted by domain.                                                                                                                                                                                 | The _cloud_ folder contains AWS, Azure, and Google Cloud content.    |
| `demo_<playbook_name>.yml`     | Playbooks that start with `demo_*` are the initial Ansible example to use in the demo.                                                                                                                                 | [demo_provision_ec2_instance.yml](./playbooks/cloud/aws/demo_provision_ec2_instance.yml) located in the _cloud/aws_ folder. |
| `prepare_<playbook_name>.yml`  | Playbooks that start with `prepare_*` prepares the environment for the demo.                                                                                                                                           |[prepare_aws_environment.yml](./playbooks/cloud/aws/prepare_aws_environment.yml) located in the _cloud/aws_ folder.     |
| `README.md`                    | Contains a GIF and step-by-step instructions to prepare and perform the demo.                                                                                                                                          | [README.md](./playbooks/cloud/aws/README.md) for AWS EC2 demo.                                       |
| `solution_<playbook_name>.yml` | Playbooks that start with  `solution_*` have the tested, desired suggestion outputs. Use the tested Ansible content to compare your Ansible Lightspeed-generated outputs before the demo. | [solution_aws_environment.yml](./playbooks/cloud/aws/solution_provision_ec2_instance.yml) located in the _cloud/aws_ folder.    |

## ❗️Test before doing a demo if you're using this content locally

The model continues to improve and evolve with each release. This can result in generated suggestions that differ from the examples provided.

Tested Ansible Playbooks are available for each corresponding demo Playbook thats starts with the `solution_*.yml` prefix. For example, `solution_provision_azure_vm.yml`.  
Please use this to compare your generated suggestions before doing the demo.

## How can I contribute?

Please refer to the [Contributing](./docs/contributing.md) guide for more information.

---
