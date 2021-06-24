# Azure CLI commands 

### To get the supported locations of desired resource types

The resource group location can be different of provisioning resources. Some of the resource types can not be provisioned in every location. The following command will list the locations of your desired resource types so that you can opt the location as per your convenience.

Example: Microsoft Azure Batch service

```
az provider show --namesapce Microsoft.Batch \
                 --query "resourceTypes[?resourceType=='batchAccounts'].location" \
                 --out Table
```