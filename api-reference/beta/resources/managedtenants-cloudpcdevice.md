---
title: "cloudPcDevice resource type"
description: "Represents a cloud-managed virtual desktop."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# cloudPcDevice resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a cloud-managed virtual desktop.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List cloudPcDevices](../api/managedTenants-cloudpcdevice-list.md)|[cloudPcDevice](../resources/managedTenants-cloudpcdevice.md) collection|Get a list of the [cloudPcDevice](../resources/managedTenants-cloudpcdevice.md) objects and their properties.|
|[Get cloudPcDevice](../api/managedTenants-cloudpcdevice-get.md)|[cloudPcDevice](../resources/managedTenants-cloudpcdevice.md)|Read the properties and relationships of a [cloudPcDevice](../resources/managedTenants-cloudpcdevice.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|displayName|String|The display name for the cloud PC.|
|id|String|The unique identifier for this entity.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|managedDeviceId|String|The device identifier from Intune for the cloud PC.|
|managedDeviceName|String|THe display name from Intune for the cloud PC|
|policyId|String|The provisioning policy identifier for the cloud PC.|
|servicePlanName|String|The service plan name for the cloud PC.|
|status|String|Status of the cloud PC. Possible values are: `notProvisioned`, `provisioning`, `provisioned`, `upgrading`, `inGracePeriod`, `deprovisioning`, `failed`.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The unique identifier for the managed tenant.|
|userPrincipalName|String|The user principal name (UPN) of the user assigned to the cloud PC.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.cloudPcDevice",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.cloudPcDevice",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "displayName": "String",
  "managedDeviceId": "String",
  "managedDeviceName": "String",
  "userPrincipalName": "String",
  "servicePlanName": "String",
  "status": "String",
  "lastRefreshedDateTime": "String (timestamp)",
  "policyId": "String"
}
```
