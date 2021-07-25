# gh-terraform-deploy-action
Simple and minimal GitHub action to deploy Terraform code.

On pull requests, it will run the following. When complete, a comment will be generated.
* terraform fmt -check
* terraform init
* terraform validate
* terraform plan

On push to master, the following will run contingent that the previous steps succeeded.
* terraform apply -auto-approve
