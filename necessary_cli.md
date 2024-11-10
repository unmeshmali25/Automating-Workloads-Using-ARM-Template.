> ssh key for deploying ARM template at runtime since we have defined it as a parameter
`ssh-keygen -t rsa -b 2048 -f ~/.ssh/my_ssh_key -C "odl_user_1476152@simplilearnhol15.onmicrosoft.com"`
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1bmMWIe4sEQkmZNcM16mUKzV/DrldwaTz3Clchx3weq8qihV+5F2I/******/uUAK3vDQLgQI+UUbTwKhgghEihLi6ZYvR+IAFN3jOxbth63AZ6EGw2GmtLGHdCmyVqu3N6p7sdKwjfXqRwdbOwNj6MKvPpGoiFm00CL6WohyxjLo9HWrM5kSYbRqgZfR8KvdqjgTjzHa8rprUAPysxAPFuz7T/yoGImw1H5ZWrNk***************6A/9s9jVuanKaIcdr4znyG2yY7zrBXxOfPeMg12EAgjIHWJhszofuVNnGDJEWikL3g1IZ6vr odl_user_1476152@simplilearnhol15.onmicrosoft.com
```

> Create resource group
`az group create --name umRandResourceGroup --location eastus`

> List all resource groups in the subscription
`   az group list --query "[].name" -o table`

> Delete all resources within a resource group
`   az resource delete --resource-group myResourceGroup --ids $(az resource list --resource-group myResourceGroup --query "[].id" -o tsv)`

> Deploy ARM template
`az deployment group create --resource-group umRandResourceGroup --template-file azuredeploy.json --parameters sshPublicKey="your-ssh-public-key"`

