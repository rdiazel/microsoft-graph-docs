---
title: "managementTemplate resource type"
description: "Represents the group of actions and settings used to perform a specific set of actions or configurations on a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managementTemplate resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the group of actions and settings used to perform a specific set of actions or configurations on a managed tenant.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List managementTemplates](../api/managedtenants-managementtemplate-list.md)|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md) collection|Get a list of the [managementTemplate](../resources/managedtenants-managementtemplate.md) objects and their properties.|
|[Get managementTemplate](../api/managedtenants-managementtemplate-get.md)|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md)|Read the properties and relationships of a [managementTemplate](../resources/managedtenants-managementtemplate.md) object.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|category|managementCategory|The category of the management template. Possible values are: `devices`, `identity`, `custom`, `unknownFutureValue`.|
|description|String|The description of the management template.|
|displayName|String|The display name of the management template.|
|id|String|The unique identifier of the management template.|
|parameters|[microsoft.graph.managedTenants.templateParameter](../resources/managedtenants-templateparameter.md) collection|A collection of parameters used by the management template.|
|workloadActions|[microsoft.graph.managedTenants.workloadAction](../resources/managedtenants-workloadaction.md) collection|A collection of workload actions that will be performed by the management template.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managementTemplate",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplate",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "parameters": [
    {
      "@odata.type": "microsoft.graph.managedTenants.templateParameter"
    }
  ],
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
    }
  ]
}
```
