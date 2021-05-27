---
title: "cloudPcConnection resource type"
description: "Represents a defined collection of Azure resource information that can be used to establish on-premises network connectivity for cloud PCs."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# cloudPcConnection resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a defined collection of Azure resource information that can be used to establish on-premises network connectivity for cloud PCs.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List cloudPcConnections](../api/managedTenants-cloudpcconnection-list.md)|[cloudPcConnection](../resources/managedTenants-cloudpcconnection.md) collection|Get a list of the [cloudPcConnection](../resources/managedtenants-cloudpcconnection.md) objects and their properties.|
|[Get cloudPcConnection](../api/managedTenants-cloudpcconnection-get.md)|[cloudPcConnection](../resources/managedTenants-cloudpcconnection.md)|Read the properties and relationships of a [cloudPcConnection](../resources/managedTenants-cloudpcconnection.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|displayName|String|The display name of the cloud PC connection.|
|healthCheckStatus|String|Status of the cloud PC. Possible values are: `pending`, `running`, `passed`, `failed`, `unknownFutureValue`.|
|id|String|The unique identifier for this entity.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The unique identifier for the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.cloudPcConnection",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.cloudPcConnection",
  "id": "String (identifier)",
  "displayName": "String",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "healthCheckStatus": "String",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
