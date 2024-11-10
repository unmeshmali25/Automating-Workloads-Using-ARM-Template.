The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
MACFG33C2C21M:Azure-ARM c536898$ 
 *  History restored 


The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
MACFG33C2C21M:Azure-ARM c536898$ az login
A web browser has been opened at https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize. Please continue the login in the web browser. If no web browser is available or if the web browser fails to open, use device code flow with `az login --use-device-code`.
[
  {
    "cloudName": "AzureCloud",
    "homeTenantId": "49947173-02e2-4471-8bed-3eb931aa77af",
    "id": "77ff16ae-64fc-4e19-954b-fc0040b17579",
    "isDefault": true,
    "managedByTenants": [],
    "name": "Simplilearn HOL 67",
    "state": "Enabled",
    "tenantId": "49947173-02e2-4471-8bed-3eb931aa77af",
    "user": {
      "name": "odl_user_1476152@simplilearnhol67.onmicrosoft.com",
      "type": "user"
    }
  }
]
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$    ssh-keygen -t rsa -b 2048 -f ~/.ssh/my_ssh_key -C "odl_user_1476152@simplilearnhol15.onmicrosoft.com"
Generating public/private rsa key pair.
/Users/c536898/.ssh/my_ssh_key already exists.
Overwrite (y/n)? y
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/c536898/.ssh/my_ssh_key
Your public key has been saved in /Users/c536898/.ssh/my_ssh_key.pub
The key fingerprint is:
SHA256:nkSQRnbm6tX0hOSFro5tWyLXpfDU8/diIFBpHQHMyvs odl_user_1476152@simplilearnhol15.onmicrosoft.com
The key's randomart image is:
+---[RSA 2048]----+
|     .+.ooo=+o   |
|     .o= oBo.    |
|     . .o=+ .    |
|       o+o.+     |
|      . S+o =    |
|     . +o*.o.o   |
|      o+=.=. .. .|
|      .o+oE   o..|
|       ...   . ..|
+----[SHA256]-----+
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ^[


{"code": "ResourceGroupNotFound", "message": "Resource group 'umRandResourceGroup' could not be found."}
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ vi ~/.ssh/my_ssh_key.pub 
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "ResourceGroupNotFound", "message": "Resource group 'umRandResourceGroup' could not be found."}
MACFG33C2C21M:Azure-ARM c536898$ az group create --name umRandResourceGroup --location eastus
{
  "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup",
  "location": "eastus",
  "managedBy": null,
  "name": "umRandResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null,
  "type": "Microsoft.Resources/resourceGroups"
}
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): az group create --name MyResourceGroup --location eastus^[





^Z
[1]+  Stopped                 az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
MACFG33C2C21M:Azure-ARM c536898$ vi ~/.ssh/my_ssh_key.pub 
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{
  "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Resources/deployments/vmtemplate",
  "location": null,
  "name": "vmtemplate",
  "properties": {
    "correlationId": "8012036a-0e48-4faa-b0d0-f83cba536ee0",
    "debugSetting": null,
    "dependencies": [
      {
        "dependsOn": [
          {
            "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/virtualNetworks/RandVNet",
            "resourceGroup": "umRandResourceGroup",
            "resourceName": "RandVNet",
            "resourceType": "Microsoft.Network/virtualNetworks"
          }
        ],
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
        "resourceGroup": "umRandResourceGroup",
        "resourceName": "RandVM1NIC",
        "resourceType": "Microsoft.Network/networkInterfaces"
      },
      {
        "dependsOn": [
          {
            "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
            "resourceGroup": "umRandResourceGroup",
            "resourceName": "RandVM1NIC",
            "resourceType": "Microsoft.Network/networkInterfaces"
          }
        ],
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Compute/virtualMachines/RandVM1",
        "resourceGroup": "umRandResourceGroup",
        "resourceName": "RandVM1",
        "resourceType": "Microsoft.Compute/virtualMachines"
      }
    ],
    "duration": "PT14.1055887S",
    "error": null,
    "mode": "Incremental",
    "onErrorDeployment": null,
    "outputResources": [
      {
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Compute/virtualMachines/RandVM1",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkSecurityGroups/RandNSG",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/virtualNetworks/RandVNet",
        "resourceGroup": "umRandResourceGroup"
      }
    ],
    "outputs": null,
    "parameters": {
      "sshPublicKey": {
        "type": "String",
        "value": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com"
      }
    },
    "parametersLink": null,
    "providers": [
      {
        "id": null,
        "namespace": "Microsoft.Network",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "virtualNetworks",
            "zoneMappings": null
          },
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "networkSecurityGroups",
            "zoneMappings": null
          },
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "networkInterfaces",
            "zoneMappings": null
          }
        ]
      },
      {
        "id": null,
        "namespace": "Microsoft.Compute",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "virtualMachines",
            "zoneMappings": null
          }
        ]
      }
    ],
    "provisioningState": "Succeeded",
    "templateHash": "14476161869227167995",
    "templateLink": null,
    "timestamp": "2024-10-05T16:11:55.630936+00:00",
    "validatedResources": null
  },
  "resourceGroup": "umRandResourceGroup",
  "tags": null,
  "type": "Microsoft.Resources/deployments"
}
MACFG33C2C21M:Azure-ARM c536898$ az group create --name umRandResourceGroup --location eastus
(ResourceGroupBeingDeleted) The resource group 'umRandResourceGroup' is in deprovisioning state and cannot perform this operation.
Code: ResourceGroupBeingDeleted
Message: The resource group 'umRandResourceGroup' is in deprovisioning state and cannot perform this operation.
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ az group create --name umRandResourceGroup --location eastus
(ResourceGroupBeingDeleted) The resource group 'umRandResourceGroup' is in deprovisioning state and cannot perform this operation.
Code: ResourceGroupBeingDeleted
Message: The resource group 'umRandResourceGroup' is in deprovisioning state and cannot perform this operation.
MACFG33C2C21M:Azure-ARM c536898$ az group create --name umRandResourceGroup --location eastus
{
  "id": "/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup",
  "location": "eastus",
  "managedBy": null,
  "name": "umRandResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null,
  "type": "Microsoft.Resources/resourceGroups"
}
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ vi ~/.ssh/my_ssh_key.pub 
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"status":"Failed","error":{"code":"DeploymentFailed","target":"/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Resources/deployments/vmtemplate","message":"At least one resource deployment operation failed. Please list deployment operations for details. Please see https://aka.ms/arm-deployment-operations for usage details.","details":[{"code":"ParentResourceNotFound","message":"Failed to perform 'write' on resource(s) of type 'storageAccounts/blobServices', because the parent resource '/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/randstorageaccount' could not be found."},{"code":"NoRegisteredProviderFound","message":"No registered resource provider found for location 'eastus' and API version '2020-06-01' for type 'storageAccounts'. The supported api-versions are '2024-01-01, 2023-05-01, 2023-04-01, 2023-01-01, 2022-09-01, 2022-05-01, 2021-09-01, 2021-08-01, 2021-06-01, 2021-05-01, 2021-04-01, 2021-02-01, 2021-01-01, 2020-08-01-preview, 2019-06-01, 2019-04-01, 2018-11-01, 2018-07-01, 2018-03-01-preview, 2018-02-01, 2017-10-01, 2017-06-01, 2016-12-01, 2016-05-01, 2016-01-01, 2015-06-15, 2015-05-01-preview'. The supported locations are 'eastus, eastus2, westus, westeurope, eastasia, southeastasia, japaneast, japanwest, northcentralus, southcentralus, centralus, northeurope, brazilsouth, australiaeast, australiasoutheast, southindia, centralindia, westindia, canadaeast, canadacentral, westus2, westcentralus, uksouth, ukwest, koreacentral, koreasouth, francecentral, australiacentral, southafricanorth, uaenorth, switzerlandnorth, germanywestcentral, norwayeast, westus3, jioindiawest, swedencentral, qatarcentral, polandcentral, italynorth, israelcentral, mexicocentral, spaincentral'."}]}}
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ^Z        
[2]+  Stopped                 az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ vi ~/.ssh/my_ssh_key.pub 
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmtemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'vmtemplate' is not valid according to the validation procedure. The tracking id is 'b68d314b-a380-4b6c-947a-60a5b154872a'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "StorageAccountAlreadyTaken", "target": "randstorageaccount", "message": "The storage account named randstorageaccount is already taken."}
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmstoragetemplate --resource-group umRandResourceGroup --template-fil
e $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'vmstoragetemplate' is not valid according to the validation procedure. The tracking id is '4ba52c6b-2448-4008-aa82-259ac8a6cff0'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "StorageAccountAlreadyTaken", "target": "randstorageaccount", "message": "The storage account named randstorageaccount is already taken."}
MACFG33C2C21M:Azure-ARM c536898$ az resource delete --resource-group umRandResourceGroup --ids $(az resource list --resource-group 
<your-resource-group-name> --query "[].id" -o tsv)
bash: your-resource-group-name: No such file or directory
argument --ids: expected at least one argument

Examples from AI knowledge base:
az resource delete --ids /subscriptions/0b1f6471-1bf0-4dda-aec3-111111111111/resourceGroups/MyResourceGroup/providers/Microsoft.Web/sites/MyWebapp
Delete a web app using a resource identifier.

az resource delete --resource-group MyResourceGroup --name MyVm --resource-type "Microsoft.Compute/virtualMachines"
Delete a virtual machine named 'MyVm'.

https://docs.microsoft.com/en-US/cli/azure/resource#az_resource_delete
Read more about the command in reference docs
MACFG33C2C21M:Azure-ARM c536898$ az resource delete --resource-group umRandResourceGroup 




--resource-type is required
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$    az group list --query "[].name" -o table
Result
-----------------------------------------
umRandResourceGroup
ODL-azure-1476152
Cloudlabs-ACI-1476152-VM-1476152-cs3afb89
NetworkWatcherRG
MACFG33C2C21M:Azure-ARM c536898$    az resource delete --resource-group umRandResourceGroup --ids $(az resource list --resource-group myResourceGroup --query "[].id" -o tsv)
ERROR: (ResourceGroupNotFound) Resource group 'myResourceGroup' could not be found.
Code: ResourceGroupNotFound
Message: Resource group 'myResourceGroup' could not be found.
argument --ids: expected at least one argument

Examples from AI knowledge base:
az resource delete --ids /subscriptions/0b1f6471-1bf0-4dda-aec3-111111111111/resourceGroups/MyResourceGroup/providers/Microsoft.Web/sites/MyWebapp
Delete a web app using a resource identifier.

az resource delete --resource-group MyResourceGroup --name MyVm --resource-type "Microsoft.Compute/virtualMachines"
Delete a virtual machine named 'MyVm'.

https://docs.microsoft.com/en-US/cli/azure/resource#az_resource_delete
Read more about the command in reference docs
MACFG33C2C21M:Azure-ARM c536898$    az resource delete --resource-group umRandResourceGroup --ids $(az resource list --resource-group umRandResourceGroup --query "[].id" -o tsv)




[
  null,
  null,
  null,
  null,
  null
]
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ 
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmstoragetemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'vmstoragetemplate' is not valid according to the validation procedure. The tracking id is '4152f393-9800-45bf-ae71-4da894e301a5'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "StorageAccountAlreadyTaken", "target": "randstorageaccount", "message": "The storage account named randstorageaccount is already taken."}
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name vmstoragetemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'vmstoragetemplate' is not valid according to the validation procedure. The tracking id is '0b36e64d-75bb-41a2-b798-8aa340cb0f37'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "StorageAccountAlreadyTaken", "target": "randstorageaccount", "message": "The storage account named randstorageaccount is already taken."}
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name um_vmstoragetemplate --resource-group umRandResourceGroup --templat
e-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'um_vmstoragetemplate' is not valid according to the validation procedure. The tracking id is '76b41444-6e0e-4ab2-b6ed-5c7c72c301f2'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "StorageAccountAlreadyTaken", "target": "randstorageaccount", "message": "The storage account named randstorageaccount is already taken."}
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name um_vmstoragetemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"code": "InvalidTemplateDeployment", "message": "The template deployment 'um_vmstoragetemplate' is not valid according to the validation procedure. The tracking id is '297dd050-099c-412d-ae35-d3a9a0360a6d'. See inner errors for details."}

Inner Errors: 
{"code": "PreflightValidationCheckFailed", "message": "Preflight validation failed. Please refer to the details for the specific errors."}

Inner Errors: 
{"code": "AccountNameInvalid", "target": "umRandStorageAccount", "message": "umRandStorageAccount is not a valid storage account name. Storage account name must be between 3 and 24 characters in length and use numbers and lower-case letters only."}
MACFG33C2C21M:Azure-ARM c536898$ templateFile="/Users/c536898/Documents/Engineering/Cloud/Projects/Azure-ARM/azuredeploy.json"
MACFG33C2C21M:Azure-ARM c536898$ az deployment group create --name um_vmstoragetemplate --resource-group umRandResourceGroup --template-file $templateFile
Please provide string value for 'sshPublicKey' (? for help): ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
{"status":"Failed","error":{"code":"DeploymentFailed","target":"/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Resources/deployments/um_vmstoragetemplate","message":"At least one resource deployment operation failed. Please list deployment operations for details. Please see https://aka.ms/arm-deployment-operations for usage details.","details":[{"code":"ParentResourceNotFound","message":"Failed to perform 'write' on resource(s) of type 'storageAccounts/blobServices', because the parent resource '/subscriptions/77ff16ae-64fc-4e19-954b-fc0040b17579/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/randstorageaccount' could not be found."}]}}
MACFG33C2C21M:Azure-ARM c536898$    az resource delete --resource-group umRandResourceGroup --ids $(az resource list --resource-group umRandResourceGroup --query "[].id" -o tsv)
[
  null,
  null,
  null,
  null,
  null,
  null
]
MACFG33C2C21M:Azure-ARM c536898$ 


# Sucessful Deployment Output
{
  "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Resources/deployments/azuredeploy",
  "location": null,
  "name": "azuredeploy",
  "properties": {
    "correlationId": "8a2f2d85-83bc-4ffd-8036-d5e620681b81",
    "debugSetting": null,
    "dependencies": [
      {
        "dependsOn": [
          {
            "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/virtualNetworks/RandVNet",
            "resourceGroup": "umRandResourceGroup",
            "resourceName": "RandVNet",
            "resourceType": "Microsoft.Network/virtualNetworks"
          }
        ],
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
        "resourceGroup": "umRandResourceGroup",
        "resourceName": "RandVM1NIC",
        "resourceType": "Microsoft.Network/networkInterfaces"
      },
      {
        "dependsOn": [
          {
            "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
            "resourceGroup": "umRandResourceGroup",
            "resourceName": "RandVM1NIC",
            "resourceType": "Microsoft.Network/networkInterfaces"
          }
        ],
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Compute/virtualMachines/RandVM1",
        "resourceGroup": "umRandResourceGroup",
        "resourceName": "RandVM1",
        "resourceType": "Microsoft.Compute/virtualMachines"
      },
      {
        "dependsOn": [
          {
            "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/umrandstorageaccountum",
            "resourceGroup": "umRandResourceGroup",
            "resourceName": "umrandstorageaccountum",
            "resourceType": "Microsoft.Storage/storageAccounts"
          }
        ],
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/umrandstorageaccountum/blobServices/default/containers/images",
        "resourceGroup": "umRandResourceGroup",
        "resourceName": "umrandstorageaccountum/default/images",
        "resourceType": "Microsoft.Storage/storageAccounts/blobServices/containers"
      }
    ],
    "duration": "PT34.2341859S",
    "error": null,
    "mode": "Incremental",
    "onErrorDeployment": null,
    "outputResources": [
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Authorization/roleAssignments/f3937e46-c504-5875-91c6-da4276b16b23",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Compute/virtualMachines/RandVM1",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkInterfaces/RandVM1NIC",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/networkSecurityGroups/RandNSG",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Network/virtualNetworks/RandVNet",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/umrandstorageaccountum",
        "resourceGroup": "umRandResourceGroup"
      },
      {
        "id": "/subscriptions/1c6f2739-fd08-4ed7-803e-3fa4bcc9320c/resourceGroups/umRandResourceGroup/providers/Microsoft.Storage/storageAccounts/umrandstorageaccountum/blobServices/default/containers/images",
        "resourceGroup": "umRandResourceGroup"
      }
    ],
    "outputs": null,
    "parameters": {
      "operationsTeamPrincipalId": {
        "type": "String",
        "value": "c1aa5f88-ce88-4e25-9cf6-e1e3489d233a"
      },
      "roleDefinitionId": {
        "type": "String",
        "value": "bd80684d-2f5f-4130-892a-0955546282de"
      },
      "sshPublicKey": {
        "type": "String",
        "value": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/gXtMsZMBcQO/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk+dn9GgUge9j16qNU6itxK6i5Q8yU2be6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com"
      }
    },
    "parametersLink": null,
    "providers": [
      {
        "id": null,
        "namespace": "Microsoft.Network",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "virtualNetworks",
            "zoneMappings": null
          },
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "networkSecurityGroups",
            "zoneMappings": null
          },
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "networkInterfaces",
            "zoneMappings": null
          }
        ]
      },
      {
        "id": null,
        "namespace": "Microsoft.Compute",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "virtualMachines",
            "zoneMappings": null
          }
        ]
      },
      {
        "id": null,
        "namespace": "Microsoft.Storage",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              "eastus"
            ],
            "properties": null,
            "resourceType": "storageAccounts",
            "zoneMappings": null
          },
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              null
            ],
            "properties": null,
            "resourceType": "storageAccounts/blobServices/containers",
            "zoneMappings": null
          }
        ]
      },
      {
        "id": null,
        "namespace": "Microsoft.Authorization",
        "providerAuthorizationConsentState": null,
        "registrationPolicy": null,
        "registrationState": null,
        "resourceTypes": [
          {
            "aliases": null,
            "apiProfiles": null,
            "apiVersions": null,
            "capabilities": null,
            "defaultApiVersion": null,
            "locationMappings": null,
            "locations": [
              null
            ],
            "properties": null,
            "resourceType": "roleAssignments",
            "zoneMappings": null
          }
        ]
      }
    ],
    "provisioningState": "Succeeded",
    "templateHash": "5433927529467066531",
    "templateLink": null,
    "timestamp": "2024-11-10T20:55:43.818193+00:00",
    "validatedResources": null
  },
  "resourceGroup": "umRandResourceGroup",
  "tags": null,
  "type