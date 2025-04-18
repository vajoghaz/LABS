Design a solution that automatically generates a new key in SQL and stores it in the key vault whenever the key vault requires a key rotation

Event Grid can capture key rotation events from Key Vault and trigger an Azure function to generate a new key in SQL and store it in Key Vault. A web app can get events from Event Grid to create and rotate a key, but it costs more than using a Azure Functions. Log Analytics cannot trigger a function.

https://learn.microsoft.com/azure/key-vault/secrets/tutorial-rotation

https://learn.microsoft.com/training/modules/azure-key-vault/




