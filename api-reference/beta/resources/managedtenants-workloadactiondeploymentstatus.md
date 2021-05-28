---
title: "workloadActionDeploymentStatus resource type"
description: "Represents the deployment status for a workload action."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# workloadActionDeploymentStatus resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the deployment status for a workload action.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|actionId|String|The identifier of the workload action.|
|deployedPolicyId|String|The identifier of the deployed policy.|
|lastDeploymentDateTime|DateTimeOffset|The date and time the deployment status was last updated.|
|status|workloadActionStatus|The deployment status of the workload action. Possible values are: `toAddress`, `completed`, `error`, `timeOut`, `inProgress`, `unknownFutureValue`.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.workloadActionDeploymentStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.workloadActionDeploymentStatus",
  "actionId": "String",
  "status": "String",
  "deployedPolicyId": "String",
  "lastDeploymentDateTime": "String (timestamp)"
}
```
