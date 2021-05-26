---
title: "conditionalAccessPolicyCoverage resource type"
description: "Represents a view of the state for each conditional access policy for each managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# conditionalAccessPolicyCoverage resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a view of the state for each conditional access policy for each managed tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List conditionalAccessPolicyCoverages](../api/managedTenants-conditionalaccesspolicycoverage-list.md)|[conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md) collection|Get a list of the [conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md) objects and their properties.|
|[Get conditionalAccessPolicyCoverage](../api/managedTenants-conditionalaccesspolicycoverage-get.md)|[conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md)|Read the properties and relationships of a [conditionalAccessPolicyCoverage](../resources/managedTenants-conditionalaccesspolicycoverage.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|conditionalAccessPolicyState|String|Specifies the state of the conditional access policy.|
|id|String|The unique identifier for the managed tenant.|
|latestPolicyModifiedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|tenantDisplayName|String|Display name for the managed tenant.|
|requiresDeviceCompliance|Boolean|A flag that determines whether a device compliance policy exists that requires compliance.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.conditionalAccessPolicyCoverage",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.conditionalAccessPolicyCoverage",
  "id": "String (identifier)",
  "tenantDisplayName": "String",
  "conditionalAccessPolicyState": "String",
  "requiresDeviceCompliance": "Boolean",
  "latestPolicyModifiedDateTime": "String (timestamp)"
}
```
