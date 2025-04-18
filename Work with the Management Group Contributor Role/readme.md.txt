1 # https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/design-area/resource-org-management-groups
2 # Create two test resource groups
3 # These operations represent Azure role-based access control (Azure RBAC) permissions. They only allow a user to read and update the hierarchy settings. They don't provide any other access to the management group hierarchy or to resources in the hierarchy ( https://learn.microsoft.com/en-us/azure/governance/management-groups/how-to/protect-resource-hierarchy#azure-rbac-permissions-for-hierarchy-settings )
Configuring hierarchy settings requires the following resource provider operations on the root management group:

Microsoft.Management/managementgroups/settings/write
Microsoft.Management/managementgroups/settings/read

Needs Entra P1 or P2 to have custom roles to include for the Management Contributor Role that originally only contains:
{
    "id": "/providers/Microsoft.Authorization/roleDefinitions/5d58bcaf-24a5-4b20-bdb6-eed9f69fbe4c",
    "properties": {
        "roleName": "Management Group Contributor",
        "description": "Management Group Contributor Role",
        "assignableScopes": [
            "/"
        ],
        "permissions": [
            {
                "actions": [
                    "Microsoft.Management/managementGroups/delete",
                    "Microsoft.Management/managementGroups/read",
                    "Microsoft.Management/managementGroups/subscriptions/delete",
                    "Microsoft.Management/managementGroups/subscriptions/write",
                    "Microsoft.Management/managementGroups/write",
                    "Microsoft.Management/managementGroups/subscriptions/read",
                    "Microsoft.Authorization/*/read"
                ],
                "notActions": [],
                "dataActions": [],
                "notDataActions": []
            }
        ]
    }