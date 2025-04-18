When deploying an AKS cluster, local accounts are enabled by default. Even when enabling RBAC or Microsoft Entra integration, --admin access still exists essentially as a non-auditable backdoor option. To disable local accounts on an AKS cluster, you should use the --disable-local-accounts flag with the az aks create command. The remaining options do not remove local accounts.

https://learn.microsoft.com/en-us/azure/aks/manage-local-accounts-managed-azure-ad

add to AGIC lab

