# Terraform Core Workflow
- terraform init
    - Usually first command that we run when we clone any existing configuration or start writing new configuration 
    - Used to initialize terraform(Backend, download required plugins) in the current working directory
    - Can be run more than once. It never modifies state file

- terraform validate
    - Validate configuration files (Whether they are syntactically correct - attribute names, value data types etc.)
    
- terraform plan
    - This command loads the existing state file (Either local or remote backend) in memory and compares the configuration against the cloud provider and creates an execution plan
    - Shows xx to add, yy to change and zz to destroy as the output of this plan
    - We can also save this plan in a .tfplan file
    - Example - terraform plan -out samplePlan.tfPlan

- terraform apply
    - Execute all actions that were proposed in terraform plan

- terraform destroy
    - Destroys resources