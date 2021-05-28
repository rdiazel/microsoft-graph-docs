---
title: "templateParameter resource type"
description: "Represents a parameter for a management template."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# templateParameter resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a parameter for a management template.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|description|String|The description of the management template parameter.|
|displayName|String|The display name of the management template parameter.|
|jsonAllowedValues|String|The allowed values of the management template parameter represented as a serialized string of JSON.|
|jsonDefaultValue|String|The default value of the management template parameter represented as a serialized string of JSON.|
|valueType|managementParameterValueType|The parameter type of the management template parameter. Possible values are: `string`, `integer`, `boolean`, `guid`, `stringCollection`, `integerCollection`, `booleanCollection`, `guidCollection`, `unknownFutureValue`.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.templateParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.templateParameter",
  "displayName": "String",
  "description": "String",
  "valueType": "String",
  "jsonDefaultValue": "String",
  "jsonAllowedValues": "String"
}
```
