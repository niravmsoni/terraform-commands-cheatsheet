# Terraform Core Workflow
- terraform init
    - Usually first command that we run when we clone any existing configuration or start writing new configuration 
    - Used to initialize terraform(Backend, download required plugins) in the current working directory
    - Can be run more than once. It never modifies state file
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/c009dde9-45fd-4711-aaef-ca8a2e336912)

- terraform validate
    - Validate configuration files (Whether they are syntactically correct - attribute names, value data types etc.)
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/dc6f0257-3058-417a-b9af-56a0783eb653)

- terraform plan
    - This command loads the existing state file (Either local or remote backend) in memory and compares the configuration against the cloud provider and creates an execution plan
    - Shows xx to add, yy to change and zz to destroy as the output of this plan
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/03d20d73-df51-4d87-9789-981bdf9dc36f)
    - We can also save this plan in a .tfplan file
    - Example - terraform plan -out samplePlan.tfPlan
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/105381ac-5bb6-4011-8ff0-6d5cccf14e35)

- terraform apply
    - Execute all actions that were proposed in terraform plan
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/56db161e-21ce-4cad-86b9-f89628dcda73)

- terraform destroy
    - Destroys resources
    - ![image](https://github.com/niravmsoni/terraform-commands-cheatsheet/assets/6556021/b2f80a52-d978-4c75-b7c8-27ad113d1a33)

