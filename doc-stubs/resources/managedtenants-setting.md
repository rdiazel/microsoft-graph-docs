---
title: "setting resource type"
description: "Represents a setting performed when a management action is applied."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# setting resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a setting performed when a management action is applied.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|displayName|String|The display name of the setting.|
|jasonValue|String|The value of the setting represented by a serialized string of JSON.|
|overwriteAllowed|Boolean|A flag indicating whether overwrites are allowed. If true the value of the setting can be overwritten.|
|valueType|managementParameterValueType|The type of the setting value. Possible values are: `string`, `integer`, `boolean`, `guid`, `stringCollection`, `integerCollection`, `booleanCollection`, `guidCollection`, `unknownFutureValue`.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.setting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.setting",
  "displayName": "String",
  "overwriteAllowed": "Boolean",
  "valueType": "String",
  "jasonValue": "String"
}
```
