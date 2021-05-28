---
title: "managementTemplateDetailedInfo resource type"
description: "Represent detailed information for a management template."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# managementTemplateDetailedInfo resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represent detailed information for a management template.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|category|managementCategory|The category of the management template. Possible values are: `devices`, `identity`, `custom`, `unknownFutureValue`.|
|displayName|String|The display name of the management template.|
|managementTemplateId|String|The identifier of the management template.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.managementTemplateDetailedInfo"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplateDetailedInfo",
  "managementTemplateId": "String",
  "displayName": "String",
  "category": "String"
}
```
