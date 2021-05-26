---
title: "managedDeviceComplianceTrend resource type"
description: "Represents an aggregate of compliant and non-compliant managed device trends for all managed tenants."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# managedDeviceComplianceTrend resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an aggregate of compliant and non-compliant managed device trends for all managed tenants.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedDeviceComplianceTrends](../api/managedTenants-manageddevicecompliancetrend-list.md)|[managedDeviceComplianceTrend](../resources/managedTenants-manageddevicecompliancetrend.md) collection|Get a list of the [managedDeviceComplianceTrend](../resources/managedTenants-manageddevicecompliancetrend.md) objects and their properties.|
|[Get managedDeviceComplianceTrend](../api/managedTenants-manageddevicecompliancetrend-get.md)|[managedDeviceComplianceTrend](../resources/managedTenants-manageddevicecompliancetrend.md)|Read the properties and relationships of a [managedDeviceComplianceTrend](../resources/managedTenants-manageddevicecompliancetrend.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|compliantDeviceCount|Int32|The count of devices on the managed tenant which have an 'compliant' state.|
|configManagerDeviceCount|Int32|The count of devices on the managed tenant which qualify as a 'config manager'.|
|countDateTime|String|The date and time that the compliance count was performed for this managed tenant.|
|errorDeviceCount|Int32|The count of devices on the managed tenant which have are in an 'error' state.|
|id|String|The unique identifier for this entity.|
|inGracePeriodDeviceCount|Int32|The count of devices on the managed tenant which have are still in their compliance grace period.|
|noncompliantDeviceCount|Int32|The count of devices on the managed tenant which have a 'noncompliant' state.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The unique identifier for the managed tenant.|
|unknownDeviceCount|Int32|The count of devices on the managed tenant which have an unknown compliance state.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedDeviceComplianceTrend",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedDeviceComplianceTrend",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "unknownDeviceCount": "Integer",
  "compliantDeviceCount": "Integer",
  "noncompliantDeviceCount": "Integer",
  "errorDeviceCount": "Integer",
  "inGracePeriodDeviceCount": "Integer",
  "configManagerDeviceCount": "Integer",
  "countDateTime": "String"
}
```
