# aks-provisioning

This file is to explain the steps for AKS provisioning using Terraform

Steps:
1. Login to your Azure acccount, using az login and then provide your credentials or use browser login

2. Create service principal using:
az ad sp create-for-rbac 

3. Create a main.tf having details about provider

4. Create k8s.tf having details about kubernetes cluster

5. Apart from provisioing kubernetes cluster and related resources, this config file will also provision Azure storage account and a file share. this will be used by our application for persistent storage

6. Create variables.tf file for variable declaration and default values

7. Create terraform.tfvars for assigning values to variables:

	a. client_id = app_id of your service principal

	b. client_secret = password from your service principal

8. Create a terraform.gitignore to ignore secret files(tfstate, .terraform folder, tfvars file etc)

9. Run terraform init

10. Run terraform plan

11. Run terraform apply
