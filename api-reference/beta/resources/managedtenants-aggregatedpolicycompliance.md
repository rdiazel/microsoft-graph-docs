---
title: "aggregatedPolicyCompliance resource type"
description: "Represents an aggregated device compliance policy that provides insight into the compliance state of all the configured device compliance policies across managed tenants."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# aggregatedPolicyCompliance resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an aggregated device compliance policy that provides insight into the compliance state of all the configured device compliance policies across managed tenants.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List aggregatedPolicyCompliances](../api/managedTenants-aggregatedpolicycompliance-list.md)|[aggregatedPolicyCompliance](../resources/managedTenants-aggregatedpolicycompliance.md) collection|Get a list of the [aggregatedPolicyCompliance](../resources/managedTenants-aggregatedpolicycompliance.md) objects and their properties.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|compliancePolicyId|String|The identifier of the compliance policy.|
|compliancePolicyName|String|The name of the compliance policy.|
|compliancePolicyPlatform|String|The platform type for the compliance policy.|
|compliancePolicyType|String|The type of compliance policy.|
|id|String|The unique identifier for this entity.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|numberOfCompliantDevices|Int64|Number of devices in compliant state for this policy.|
|numberOfErrorDevices|Int64|Number of devices in error state for this policy.|
|numberOfNonCompliantDevices|Int64|Number of devices in non-compliant state for this policy.|
|policyModifiedDateTime|DateTimeOffset|The last recorded update of this policy.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The Azure Active Directory tenant identifier for the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.aggregatedPolicyCompliance",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.aggregatedPolicyCompliance",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "compliancePolicyId": "String",
  "compliancePolicyName": "String",
  "compliancePolicyType": "String",
  "compliancePolicyPlatform": "String",
  "numberOfCompliantDevices": "Integer",
  "numberOfNonCompliantDevices": "Integer",
  "numberOfErrorDevices": "Integer",
  "policyModifiedDateTime": "String (timestamp)",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
