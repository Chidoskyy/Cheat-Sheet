# Terraform Infrastructure Commands

This README provides a quick reference for commonly used Terraform commands.

## Core Workflow

* `terraform init`: Initializes the working directory (downloads providers, sets up backend, modules).
* `terraform plan`: Shows proposed infrastructure changes.
* `terraform apply`: Applies the changes to create/modify/destroy infrastructure.
* `terraform destroy`: Deletes Terraform-managed infrastructure.

## State Management

* `terraform state list`: Lists resources in the current state.
* `terraform state show <address>`: Shows details of a specific resource in the state.
* `terraform state pull`: Downloads the current state.
* `terraform state push <path>`: Uploads a local state (use with caution).
* `terraform state rm <address>`: Removes a resource from the state.
* `terraform state mv <source> <destination>`: Moves a resource within the state.

## Inputs

* `terraform apply -var='<name>=<value>'`: Applies with a specific input variable value.
* `terraform apply -var-file="<filename>.tfvars"`: Applies using values from a `.tfvars` file.
* `terraform plan -var='<name>=<value>'`: Plans with a specific input variable value.
* `terraform plan -var-file="<filename>.tfvars"`: Plans using values from a `.tfvars` file.

## Outputs

* `terraform output`: Displays values of output variables.
* `terraform output <name>`: Displays the value of a specific output variable.

## Other Useful Commands

* `terraform fmt`: Formats configuration files.
* `terraform validate`: Validates configuration syntax.
* `terraform version`: Shows the Terraform version.