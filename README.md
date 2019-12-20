# Using Ansible with Azure

### Prerequisites

* *[Azure subscription](https://azure.microsoft.com/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio)*

* *[Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-3.2.0)*

* *Azure Service Principal*
    * [Create an Azure service principal with Azure CLI](https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli?view=azure-cli-latest)
    * [Create an Azure service principal with Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/create-azure-service-principal-azureps?view=azps-3.2.0)

* *Ansible Environment*
    * Linux Container
        * [Ansible Ops Box]()
    * Linux Virtual Machine
        * [Ansible Solution Template](https://docs.microsoft.com/en-us/azure/ansible/ansible-deploy-solution-template)
        * [Install Ansible on an Azure Linux virtual machine](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/ansible-install-configure?toc=%2Fazure%2Fansible%2Ftoc.json&bc=%2Fazure%2Fbread%2Ftoc.json#install-ansible-on-an-azure-linux-virtual-machine)

### [Connect to Azure from Ansible](https://dev.to/joshduffney/connecting-to-azure-with-ansible-22g2)

*Required Information*

* _Subscription Id_
* _Service Principal AppId_
* _Service Principal Password_
* _Tenant Id for the Service Principal_

### Option One: Credentials File

1. Create a credentials file
    ```bash
    mkdir ~/.azure
    vi ~/.azure/credentials
    ```
2. Populate the required Ansible variables. Replace <Text> with actual values.
    ```bash
    [default]
    subscription_id=<subscription_id>
    client_id=<security-principal-appid>
    secret=<security-principal-password>
    tenant=<security-principal-tenant>
    ```

### Option Two: Environment Variables

```
export AZURE_SUBSCRIPTION_ID=<your-subscription_id>
export AZURE_CLIENT_ID=<security-principal-appid>
export AZURE_SECRET=<security-principal-password>
export AZURE_TENANT=<security-principal-tenant>
```

### 