---
title: "workloadStatus resource type"
description: "Represent the on boarding status for a given Microsoft 365 service supported by the management platform."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# workloadStatus resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represent the on boarding status for a given Microsoft 365 service supported by the management platform.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|displayName|String|The display of the workload associated with this status.|
|offboardedDateTime|DateTimeOffset|The date and time the workload was off boarded.|
|onboardedDateTime|DateTimeOffset|The date and time the workload was on boarded.|
|onboardingStatus|workloadOnboardingStatus|The on boarding status of the workload. Possible values are: `notOnboarded`, `onboarded`, `unknownFutureValue`.|

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
