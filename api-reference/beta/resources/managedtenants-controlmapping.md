---
title: "controlMapping resource type"
description: "Represents the mapping between the action being performed and an external control."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# controlMapping resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the mapping between the action being performed and an external control.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|controlMappingId|String|The identifier of the control mapping.|
|link|String|The website containing additional information for the external control.|
|source|String|The source platform for the external control.|
|steps|String collection|An array of string that represent the steps to perform the action.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.controlMapping"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.controlMapping",
  "controlMappingId": "String",
  "link": "String",
  "source": "String",
  "steps": [
    "String"
  ]
}
```
