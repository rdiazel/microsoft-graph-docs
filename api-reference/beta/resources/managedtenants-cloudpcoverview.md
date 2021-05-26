---
title: "cloudPcOverview resource type"
description: "Represents an overview of cloud PCs for each managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# cloudPcOverview resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an overview of cloud PCs for each managed tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List cloudPcOverviews](../api/managedTenants-cloudpcoverview-list.md)|[cloudPcOverview](../resources/managedTenants-cloudpcoverview.md) collection|Get a list of the [cloudPcOverview](../resources/managedTenants-cloudpcoverview.md) objects and their properties.|
|[Get cloudPcOverview](../api/managedTenants-cloudpcoverview-get.md)|[cloudPcOverview](../resources/managedTenants-cloudpcoverview.md)|Read the properties and relationships of a [cloudPcOverview](../resources/managedTenants-cloudpcoverview.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier for the managed tenant.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|numberOfCloudPcConnectionStatusFailed|Int32|Number of cloud PC connections in `failed` state. |
|numberOfCloudPcConnectionStatusPassed|Int32|Number of cloud PC connections in `passed` state. |
|numberOfCloudPcConnectionStatusPending|Int32|Number of cloud PC connections in `pending` state.|
|numberOfCloudPcConnectionStatusRunning|Int32|Number of cloud PC connections in `running` state.|
|numberOfCloudPcConnectionStatusUnkownFutureValue|Int32|Number of cloud PC connections in `unknown future value` state.|
|numberOfCloudPcStatusDeprovisioning|Int32|Number of cloud PCs in `deprovisioning` state. |
|numberOfCloudPcStatusFailed|Int32|Number of cloud PCs in `failed` state.|
|numberOfCloudPcStatusInGracePeriod|Int32|Number of cloud PCs in `in grace period` state.|
|numberOfCloudPcStatusNotProvisioned|Int32|Number of cloud PCs in `not provisioned` state.|
|numberOfCloudPcStatusProvisioned|Int32|Number of cloud PCs in `provisioned` state.|
|numberOfCloudPcStatusProvisioning|Int32|Number of cloud PCs in `provisioning` state.|
|numberOfCloudPcStatusUnknown|Int32|Number of cloud PCs in `unknown` state.|
|numberOfCloudPcStatusUpgrading|Int32|Number of cloud PCs in `upgrading` state.|
|tenantDisplayName|String|Display name for the managed tenant.|
|totalCloudPcConnectionStatus|Int32|Number of cloud PC connection statuses in all managed tenants.|
|totalCloudPcStatus|Int32|Number of cloud PC statuses in all managed tenants.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.cloudPcOverview",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.cloudPcOverview",
  "id": "String (identifier)",
  "tenantDisplayName": "String",
  "totalCloudPcStatus":"Integer",
  "numberOfCloudPcStatusNotProvisioned":"Integer",
  "numberOfCloudPcStatusProvisioning":"Integer",
  "numberOfCloudPcStatusProvisioned":"Integer",
  "numberOfCloudPcStatusUpgrading":"Integer",
  "numberOfCloudPcStatusInGracePeriod":"Integer",
  "numberOfCloudPcStatusDeprovisioning":"Integer",
  "numberOfCloudPcStatusFailed":"Integer",
  "numberOfCloudPcStatusUnknown":"Integer",
  "totalCloudPcConnectionStatus":"Integer",
  "numberOfCloudPcConnectionStatusPending":"Integer",
  "numberOfCloudPcConnectionStatusRunning":"Integer",
  "numberOfCloudPcConnectionStatusPassed":"Integer",
  "numberOfCloudPcConnectionStatusFailed":"Integer",
  "numberOfCloudPcConnectionStatusUnkownFutureValue":"Integer",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
