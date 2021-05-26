---
title: "managementIntent resource type"
description: "Represents the intent to manage a group of managed tenants."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managementIntent resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the intent to manage a group of managed tenants.

Inherits from [entity](../resources/managedtenants-entity.md).

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List managementIntents](../api/managedtenants-managementintent-list.md)|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md) collection|Get a list of the [managementIntent](../resources/managedtenants-managementintent.md) objects and their properties.|
|[Get managementIntent](../api/managedtenants-managementintent-get.md)|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md)|Read the properties and relationships of a [managementIntent](../resources/managedtenants-managementintent.md) object.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|displayName|String|The display name of the management intent.|
|id|String|The unique identifier of the management intent. Inherited from [entity](../resources/managedtenants-entity.md).|
|isGlobal|Boolean|A flag indicating whether or not the management intent is global.|
|managementTemplates|[microsoft.graph.managedTenants.managementTemplateDetailedInfo](../resources/managedtenants-managementtemplatedetailedinfo.md) collection|A collection of management templates associated with the management intent.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managementIntent",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementIntent",
  "id": "String (identifier)",
  "displayName": "String",
  "isGlobal": "Boolean",
  "managementTemplates": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementTemplateDetailedInfo"
    }
  ]
}
```
