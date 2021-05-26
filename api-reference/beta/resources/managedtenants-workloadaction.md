---
title: "workloadAction resource type"
description: "Represents an action that will be performed against a Microsoft 365 service."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# workloadAction resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an action that will be performed against a Microsoft 365 service.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|actionId|String|The identifier of the workload action.|
|category|workloadActionCategory|The category of the workload action. Possible values are: `automated`, `manual`, `unknownFutureValue`.|
|description|String|The description of the workload action.|
|displayName|String|The display name of the workload action.|
|service|String|The Microsoft 365 service that owns the action to be performed.|
|settings|[microsoft.graph.managedTenants.setting](../resources/managedtenants-setting.md) collection|A collection of settings associated with the workload action.|

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
