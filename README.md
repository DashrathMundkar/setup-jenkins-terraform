# setup-jenkins-terraform

### [Setup-Jenkins-on-VM](Setup-Jenkins-on-VM/)
Terraform configuration to deploy Jenkins on an Azure Virtual Machine.
- **Files:**
  - `main.tf` - Core Azure resources (vnet, subnet, NIC, NSG)
  - `vm.tf` - Virtual machine configuration with custom script extension
  - `variable.tf` - Input variables for resource configuration
  - `DEV.tfvars` - Development environment variables
  - `output.tf` - Output values (VM public IP)
  - `jenkins_setup.sh` - Bash script to install Java 21, Git, Maven, and Jenkins
- **Key Features:** Automated Jenkins installation, SSH key-based authentication, security group rules for SSH (22), HTTP (80), HTTPS (443), and Jenkins (8080)


### For Jenkins:
```bash
cd Setup-Jenkins-on-VM
terraform init
terraform apply -var-file="DEV.tfvars"
```
