---
title: "managedTenantInfo resource type"
description: "Represents information related to a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managedTenantInfo resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents information related to a managed tenant.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|tenantId|String|The Azure Active Directory tenant identifier for a managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.managedTenantInfo"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenantInfo",
  "tenantId": "String"
}
```
