What is Terraform?

- automate the provisioning and management of infrastructure & services
- open source
- declarative language (you define the end state you desire)
- terraform will figure out the end result for you
- one tool to integrate with many technologies / apis

Ansible vs Terraform
- Both infrastructure as code
- Terraform is mainly infrastructure provisioning
- Ansible is mainly a configuration tool (once the infra is available)

Terraform is better for creating infrastructure but ansible is better for configuring that infrastructure.

Terraform "core" will compare tf-state with your config and decide what needs to be created/updated/destroyed in order to get to the desired state.

Terraform providers give you access to their resources (eg. AWS provider gives access to EC2 resources)

Commands:
- refresh (query infra provider to get current state) tf will now know the current state
- plan (take current state in your config file as the input, decide what needs to be done to achieve desired state)
- apply (execute the plan)
- destroy (destroys entire setup, removing elements 1 by 1 in the right order)