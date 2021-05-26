---
title: "deviceCompliancePolicySettingStateSummary resource type"
description: "Represents a summary of the state for a given device compliance policy setting across devices in a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# deviceCompliancePolicySettingStateSummary resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a summary of the state for a given device compliance policy setting across devices in a managed tenant.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List deviceCompliancePolicySettingStateSummaries](../api/managedTenants-devicecompliancepolicysettingstatesummary-list.md)|[deviceCompliancePolicySettingStateSummary](../resources/managedTenants-devicecompliancepolicysettingstatesummary.md) collection|Get a list of the [deviceCompliancePolicySettingStateSummary](../resources/managedTenants-devicecompliancepolicysettingstatesummary.md) objects and their properties.|
|[Get deviceCompliancePolicySettingStateSummary](../api/managedTenants-devicecompliancepolicysettingstatesummary-get.md)|[deviceCompliancePolicySettingStateSummary](../resources/managedTenants-devicecompliancepolicysettingstatesummary.md)|Read the properties and relationships of a [deviceCompliancePolicySettingStateSummary](../resources/managedTenants-devicecompliancepolicysettingstatesummary.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|conflictDeviceCount|Int32|Number of devices that are in a conflict state for the given device compliance policy.|
|errorDeviceCount|Int32|Number of devices that are in an error state for the given device compliance policy.|
|failedDeviceCount|Int32|Number of devices that are in a failed state for the given device compliance policy.|
|id|String|The unique identifier for this entity.|
|intuneAccountId|String|The identifer for the managed tenant's Microsoft Intune account.|
|intuneSettingId|String|The identifer for a specific setting in the device compliance policy.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|notApplicableDeviceCount|Int32|Number of devices where the specific device compliance policy is not applicable.|
|pendingDeviceCount|Int32|Number of devices where the device compliance policy has yet to be evaluated.|
|policyType|String|Type of the device compliance policy in Microsoft Intune.|
|settingName|String|Name of the specific device compliance setting.|
|succeededDeviceCount|Int32|Number of devices where the specific device compliance policy has successfully been applied.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The unique identifier for the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.deviceCompliancePolicySettingStateSummary",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.deviceCompliancePolicySettingStateSummary",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "intuneAccountId": "String",
  "intuneSettingId": "String",
  "policyType": "String",
  "settingName": "String",
  "pendingDeviceCount": "Integer",
  "notApplicableDeviceCount": "Integer",
  "succeededDeviceCount": "Integer",
  "failedDeviceCount": "Integer",
  "errorDeviceCount": "Integer",
  "conflictDeviceCount": "Integer",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
