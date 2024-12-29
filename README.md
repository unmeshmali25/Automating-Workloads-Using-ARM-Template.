# Azure Infrastructure Deployment for Rand Enterprises Corporation

This project demonstrates the automated deployment of a secure and efficient Azure infrastructure for Rand Enterprises Corporation using an ARM (Azure Resource Manager) template.  The infrastructure is designed to meet the operational requirements provided by the Rand Enterprises team, focusing on security, scalability, and ease of management.

## Project Overview

The primary goal of this project is to implement Infrastructure as Code (IaC) using ARM templates. This allows for consistent and repeatable deployments, simplifies management, and reduces the risk of manual errors.
Check the PDF for screenshots of successful deployments. 

Key features of the deployed infrastructure include:

* **Defined Networking Architecture:** A virtual network (RandVNet) with dedicated subnets for application and storage resources.  This segmentation enhances security and performance.
* **Secure Storage and Compute:** Storage accounts are provisioned for storing image-based content, and virtual machines (VMs) are deployed to host applications.  Access to the storage accounts is restricted using service endpoints and network ACLs, preventing public internet access.
* **Secure Communication:**  Communication between VMs and storage accounts is secured through the internal Azure network.
* **Reusable and Automated Deployment:**  The ARM template is designed for reusability and automation, allowing for efficient and consistent deployments in the future.
* **Role-Based Access Control (RBAC):**  RBAC is implemented to grant the operations team the necessary permissions to deploy and manage the resources, adhering to the principle of least privilege.

## ARM Template Structure

The ARM template is structured into the following key sections:

* **Parameters:** This section defines the input parameters for the deployment, such as SSH public keys, role definitions for RBAC, and the object ID of the operations team in Azure Active Directory.
* **Resources:** This section defines the Azure resources to be deployed, including:
    * Virtual Network (RandVNet)
    * Subnets (ApplicationSubnet, StorageSubnet)
    * Network Security Group (RandNSG)
    * Network Interfaces
    * Virtual Machines (RandVM1)
    * Storage Account (umrandstorageaccountum)
    * Blob Container (within the storage account)
    * Role Assignments


## Deployment Process

The deployment process involves the following steps:

1. **Template Creation:** Create the ARM template (`azuredeploy.json`) defining the desired infrastructure. (Included in this repository)
2. **Parameter Definition:** Define the necessary parameter values in a separate file (`azuredeploy.parameters.json`). (Example included - adapt to your environment)
3. **Deployment Execution:** Deploy the ARM template using either the Azure CLI or the Azure portal, providing the parameter file.
4. **Validation:**  After deployment, validate that the resources were created successfully and meet the specified requirements.


## Deployment using Azure CLI

```bash
az deployment group create --resource-group <your_resource_group_name> --template-file azuredeploy.json --parameters-file azuredeploy.parameters.json
Use code with caution.
Markdown
Future Considerations
Monitoring and Logging: Implement robust monitoring and logging solutions to track resource usage, performance, and security events.

Template Versioning: Use a version control system like Git to manage changes to the ARM template and track revisions.

Custom Roles: Consider creating custom roles if built-in roles don't fully meet the operational needs of the team.

Cost Optimization: Review and optimize resource utilization to minimize costs.
