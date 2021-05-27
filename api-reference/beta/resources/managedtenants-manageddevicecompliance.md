---
title: "managedDeviceCompliance resource type"
description: "Represents a view of the device compliance states for each managed device for all managed tenants."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# managedDeviceCompliance resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a view of the device compliance states for each managed device for all managed tenants.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedDeviceCompliances](../api/managedTenants-manageddevicecompliance-list.md)|[managedDeviceCompliance](../resources/managedTenants-manageddevicecompliance.md) collection|Get a list of the [managedDeviceCompliance](../resources/managedTenants-manageddevicecompliance.md) objects and their properties.|
|[Get managedDeviceCompliance](../api/managedTenants-manageddevicecompliance-get.md)|[managedDeviceCompliance](../resources/managedTenants-manageddevicecompliance.md)|Read the properties and relationships of a [managedDeviceCompliance](../resources/managedTenants-manageddevicecompliance.md) object.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|complianceStatus|String|Compliance state of the managed device. Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.|
|deviceType|String|The platform type for the managed device.|
|id|String|The unique identifier for this entity.|
|inGracePeriodUntilDateTime|DateTimeOffset|The date and time when the device compliance grace period expires for the managed device.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|lastSyncDateTime|DateTimeOffset|The date and time for when the managed device was last synchronized with Microsoft Intune.|
|managedDeviceId|String|Identifier of the managed device.|
|managedDeviceName|String|Name of the managed device.|
|manufacturer|String|The manufacturer of the managed device.|
|model|String|The model of the managed device.|
|osDescription|String|Operating system of the managed device.|
|osVersion|String|Operating system version of the managed device.|
|ownerType|String|Ownership of the device. Possible values are: `unknown`, `company`, `personal`.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The Azure Active Directory tenant identifier for the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedDeviceCompliance",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedDeviceCompliance",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "managedDeviceId": "String",
  "managedDeviceName": "String",
  "complianceStatus": "String",
  "osDescription": "String",
  "osVersion": "String",
  "lastSyncDateTime": "String (timestamp)",
  "ownerType": "String",
  "model": "String",
  "manufacturer": "String",
  "inGracePeriodUntilDateTime": "String (timestamp)",
  "lastRefreshedDateTime": "String (timestamp)",
  "deviceType": "String"
}
```
