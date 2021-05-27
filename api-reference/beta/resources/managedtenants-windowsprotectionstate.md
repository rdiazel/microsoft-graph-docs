---
title: "windowsProtectionState resource type"
description: "Represents the managed device protection for each managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# windowsProtectionState resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the managed device protection for each managed tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List windowsProtectionStates](../api/managedTenants-windowsprotectionstate-list.md)|[windowsProtectionState](../resources/managedTenants-windowsprotectionstate.md) collection|Get a list of the [windowsProtectionState](../resources/managedTenants-windowsprotectionstate.md) objects and their properties.|
|[Get windowsProtectionState](../api/managedTenants-windowsprotectionstate-get.md)|[windowsProtectionState](../resources/managedTenants-windowsprotectionstate.md)|Read the properties and relationships of a [windowsProtectionState](../resources/managedTenants-windowsprotectionstate.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|antiMalwareVersion|String|Current anti malware version.|
|attentionRequired|Boolean|A flag indicating whether the managed device requires attention.|
|deviceDeleted|Boolean|A flag indicating whether the managed device has been deleted.|
|devicePropertiesRefreshTime|DateTimeOffset|The date and time when the managed device properties were last refreshed.|
|engineVersion|String|Current endpoint protection engine's version.|
|fullScanOverdue|Boolean|A flag indicating whether a full scan is overdue.|
|fullScanRequired|Boolean|A flag indicating whether a full scan is required.|
|id|String|The unique identifier for this entity.|
|lastFullScanDateTime|DateTimeOffset|The date and time for when the last full scan was performed.|
|lastFullScanSignatureVersion|String|Last full scan signature version.|
|lastQuickScanDateTime|DateTimeOffset|The date and time for when the last quick scan was performed.|
|lastQuickScanSignatureVersion|String|Last quick scan signature version|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|lastReportedDateTime|DateTimeOffset|The date and time when the last managed device health status was reported.|
|malwareProtectionEnabled|Boolean|A flag indicating whether malware protection is enabled.|
|managedDeviceHealthState|[windowsDeviceHealthState](../resources/intune-devices-windowsdevicehealthstate.md)|Computer's state (like clean or pending full scan or pending reboot etc). Possible values are: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.|
|managedDeviceId|String|The identifier of the managed device.|
|managedDeviceName|String|The name of the managed device.|
|networkInspectionSystemEnabled|Boolean|A flag indicating whether network inspection system is enabled.|
|quickScanOverdue|Boolean|A flag indicating whether a quick scan is overdue.|
|realTimeProtectionEnabled|Boolean|A flag indicating whether real time protection is enabled.|
|rebootRequired|Boolean|A flag indicating whether a reboot is required.|
|signatureUpdateOverdue|Boolean|A flag indicating whether a signature update is overdue.|
|signatureVersion|String|Current malware definitions version.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The Azure Active Directory tenant identifier for the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.windowsProtectionState",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.windowsProtectionState",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "managedDeviceId": "String",
  "managedDeviceName": "String",
  "malwareProtectionEnabled": "Boolean",
  "managedDeviceHealthState": "String",
  "realTimeProtectionEnabled": "Boolean",
  "networkInspectionSystemEnabled": "Boolean",
  "quickScanOverdue": "Boolean",
  "fullScanOverdue": "Boolean",
  "signatureUpdateOverdue": "Boolean",
  "rebootRequired": "Boolean",
  "attentionRequired": "Boolean",
  "fullScanRequired": "Boolean",
  "engineVersion": "String",
  "signatureVersion": "String",
  "antiMalwareVersion": "String",
  "lastQuickScanDateTime": "String (timestamp)",
  "lastFullScanDateTime": "String (timestamp)",
  "lastQuickScanSignatureVersion": "String",
  "lastFullScanSignatureVersion": "String",
  "lastReportedDateTime": "String (timestamp)",
  "devicePropertiesRefreshTime": "String (timestamp)",
  "deviceDeleted": "Boolean",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
