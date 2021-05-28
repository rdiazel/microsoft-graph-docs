---
title: "managementIntentInfo resource type"
description: "Represents information related to a management intent."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# managementIntentInfo resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents information related to a management intent.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|managementIntentDisplayName|String|The display name of the management intent.|
|managementIntentId|String|The identifier of the management intent.|
|managementTemplates|[microsoft.graph.managedTenants.managementTemplateDetailedInfo](../resources/managedtenants-managementtemplatedetailedinfo.md) collection|A group of management templates associated with the management intent.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.managementIntentInfo"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managementIntentInfo",
  "managementIntentId": "String",
  "managementIntentDisplayName": "String",
  "managementTemplates": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementTemplateDetailedInfo"
    }
  ]
}
```
