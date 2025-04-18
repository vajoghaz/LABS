You can integrate a web app only to a dedicated subnet of a virtual network that does not have any connected resources. 

The subnet can have service endpoints, but subnet delegation should either not be configured or must be configured to the Microsoft.Web/serverFarms service, otherwise you will get the following error: 
"Subnet is missing a delegation to Microsoft.Web/serverFarms. Please add the delegation and try again."

https://learn.microsoft.com/en-gb/azure/app-service/configure-vnet-integration-enable