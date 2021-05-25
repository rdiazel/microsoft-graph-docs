---
title: "workloadAction resource type"
description: "**TODO: Add Description**"
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# workloadAction resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|actionId|String|**TODO: Add Description**|
|category|workloadActionCategory|**TODO: Add Description**. Possible values are: `automated`, `manual`, `unknownFutureValue`.|
|controlMapping|[microsoft.graph.managedTenants.controlMapping](../resources/managedtenants-controlmapping.md)|**TODO: Add Description**|
|dependencies|String collection|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|service|String|**TODO: Add Description**|
|settings|[microsoft.graph.managedTenants.setting](../resources/managedtenants-setting.md) collection|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.workloadAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.workloadAction",
  "actionId": "String",
  "category": "String",
  "controlMapping": {
    "@odata.type": "microsoft.graph.managedTenants.controlMapping"
  },
  "dependencies": [
    "String"
  ],
  "displayName": "String",
  "description": "String",
  "service": "String",
  "settings": [
    {
      "@odata.type": "microsoft.graph.managedTenants.setting"
    }
  ]
}
```

