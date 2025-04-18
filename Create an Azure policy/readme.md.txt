Ensure that the policy is applied whenever a new storage account is created or updated. There is no managed identity assigned to the policy initiative

https://learn.microsoft.com/en-gb/azure/governance/policy/concepts/effect-basics

We want to deny the creation or modification of a resource if the CostCenter tag is not present. Append adds a field, but it does not ensure the tag exists and is populated. Modify adds, replaces, or removes a property. DeployIfNotExists is used to deploy an existing resource.

https://learn.microsoft.com/en-gb/azure/governance/policy/tutorials/govern-tags

ensure that any resources that are missing a tag named CostCenter inherit a value from a resource group.

indexed mode ensures that the policy skips resource groups. all includes resource groups, which cannot be nested. Append and DeployIfNotExists are policy effects.

https://learn.microsoft.com/en-gb/azure/governance/policy/concepts/definition-structure-basics#resource-manager-modes

https://learn.microsoft.com/en-gb/azure/governance/policy/tutorials/govern-tags#modify-resources-to-inherit-the-costcenter-tag-when-missing

Use this for effect: "append"

"then": {
    "effect": "",
    "details": [{
        "field": "Microsoft.Storage/storageAccounts/networkAcls.ipRules",
        "value": [{
            "action": "Allow",
            "value": "134.5.0.0/21"
        }]
    }]
}
-------------------------------
Use this for effect: "deny"

01  "if": {
02      "allOf": [{
03              "field": "type",
04              "equals": "Microsoft.Resources/subscriptions/resourceGroups"
05          },
06          {
07              "field": "tags['CostCenter']",
08              "exists": false
09          }
10      ]
11  },
12  "then": {
13      "effect": ""
14  }
-------------------------------
ensure that any resources that are missing a tag named CostCenter inherit a value from a resource group:
"policyRule": {
    "if": {
        "field": "tags['CostCenter']",
        "exists": "false"
    },
    "then": {
        "effect": "modify",
        "details": {
            "roleDefinitionIds": [
                "/providers/microsoft.authorization/roleDefinitions/b24988ac-6180-42a0-ab88-20f7382dd24c"
            ],
            "operations": [{
                "operation": "addOrReplace ",
                "field": "tags['CostCenter']",
                "value": "[resourcegroup().tags['CostCenter']]"
            }]
        }
    }
}
--------------------------------








