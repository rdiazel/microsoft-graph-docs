---
title: "tenantContract resource type"
description: "Represents the contract that exists between a managed tenant and the managing entity."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenantContract resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the contract that exists between a managed tenant and the managing entity.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|contractType|String|The type of contract that exists between a managed tenant and the managing entity.|
|defaultDomainName|String|The default domain name of the managed tenant.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.tenantContract"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantContract",
  "contractType": "String",
  "defaultDomainName": "String"
}
```
