---
title: "workloadStatus resource type"
description: "**TODO: Add Description**"
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# workloadStatus resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|displayName|String|**TODO: Add Description**|
|offboardedDateTime|DateTimeOffset|**TODO: Add Description**|
|onboardedDateTime|DateTimeOffset|**TODO: Add Description**|
|onboardingStatus|workloadOnboardingStatus|**TODO: Add Description**. Possible values are: `notOnboarded`, `onboarded`, `unknownFutureValue`.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.workloadStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.workloadStatus",
  "onboardingStatus": "String",
  "onboardedDateTime": "String (timestamp)",
  "displayName": "String",
  "offboardedDateTime": "String (timestamp)"
}
```

