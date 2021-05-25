---
title: "managementAction resource type"
description: "Represents a management action that will be performed on behalf of a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managementAction resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a management action that will be performed on behalf of a managed tenant.

Inherits from [entity](../resources/managedtenants-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managementActions](../api/managedtenants-managementaction-list.md)|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md) collection|Get a list of the [managementAction](../resources/managedtenants-managementaction.md) objects and their properties.|
|[Get managementAction](../api/managedtenants-managementaction-get.md)|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md)|Read the properties and relationships of a [managementAction](../resources/managedtenants-managementaction.md) object.|
|[apply](../api/managedtenants-managementaction-apply.md)|[microsoft.graph.managedTenants.managementActionDeploymentStatus](../resources/managedtenants-managementactiondeploymentstatus.md)|Applies the management action on behalf of a managed tenant in a specific tenant group.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|category|managementCategory|The category of the management action. Possible values are: `devices`, `identity`, `custom`, `unknownFutureValue`.|
|description|String|The description of the management action.|
|displayName|String|The display name of the management action.|
|id|String|The unique identifier of the management action. Inherited from [entity](../resources/managedtenants-entity.md).|
|referenceTemplateId|String|The reference management template identifier of the management action.|
|workloadActions|[microsoft.graph.managedTenants.workloadAction](../resources/managedtenants-workloadaction.md) collection|The list of workload actions performed by the management action.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managementAction",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementAction",
  "id": "String (identifier)",
  "referenceTemplateId": "String",
  "referenceTemplateVersion": "Integer",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
    }
  ]
}
```
