---
title: "managementActionInfo resource type"
description: "Represents additional information for a management action."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managementActionInfo resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents additional information for a management action.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|managementActionId|String|The management action identifier.|
|managementTemplateId|String|The management template identifier.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.managementActionInfo"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementActionInfo",
  "managementTemplateId": "String",
  "managementTemplateVersion": "Integer",
  "managementActionId": "String"
}
```
