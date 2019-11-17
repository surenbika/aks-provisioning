# aks-provisioning

This file is to explain the steps for AKS provisioning using Terraform

Steps:
1. Login to your Azure acccount, using az login and then provide your credentials or use browser login

2. Create service principal using:
az ad sp create-for-rbac 

3. Create a main.tf having details about provider

4. Create k8s.tf having details about kubernetes cluster

5. Create variables.tf file for variable declaration and default values

6. Create terraform.tfvars for assigning values to vairables:

	a. client_id = <app_id of your service principal>

	b. client_secret = <password of your service_principal>

7. Create a terraform.gitignore to ignore secret files(tfstate, .terraform folder, tfvars file etc)

8. Run terraform init

9. Run terraform plan

10. Run terraform apply
