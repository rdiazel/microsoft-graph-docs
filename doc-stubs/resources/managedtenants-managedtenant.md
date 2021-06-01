---
title: "managedTenant resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# managedTenant resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/managedtenants-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List managedTenants](../api/managedtenants-managedtenant-list.md)|[microsoft.graph.managedTenants.managedTenant](../resources/managedtenants-managedtenant.md) collection|Get a list of the [managedTenant](../resources/managedtenants-managedtenant.md) objects and their properties.|
|[Create managedTenant](../api/managedtenants-managedtenant-create.md)|[microsoft.graph.managedTenants.managedTenant](../resources/managedtenants-managedtenant.md)|Create a new [managedTenant](../resources/managedtenants-managedtenant.md) object.|
|[Get managedTenant](../api/managedtenants-managedtenant-get.md)|[microsoft.graph.managedTenants.managedTenant](../resources/managedtenants-managedtenant.md)|Read the properties and relationships of a [managedTenant](../resources/managedtenants-managedtenant.md) object.|
|[Update managedTenant](../api/managedtenants-managedtenant-update.md)|[microsoft.graph.managedTenants.managedTenant](../resources/managedtenants-managedtenant.md)|Update the properties of a [managedTenant](../resources/managedtenants-managedtenant.md) object.|
|[Delete managedTenant](../api/managedtenants-managedtenant-delete.md)|None|Deletes a [managedTenant](../resources/managedtenants-managedtenant.md) object.|
|[List tenants](../api/managedtenants-managedtenant-list-tenants.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|Get the tenant resources from the tenants navigation property.|
|[Create tenant](../api/managedtenants-managedtenant-post-tenants.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Create a new tenant object.|
|[List tenantsCustomizedInformation](../api/managedtenants-managedtenant-list-tenantscustomizedinformation.md)|[microsoft.graph.managedTenants.tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) collection|Get the tenantCustomizedInformation resources from the tenantsCustomizedInformation navigation property.|
|[Create tenantCustomizedInformation](../api/managedtenants-managedtenant-post-tenantscustomizedinformation.md)|[microsoft.graph.managedTenants.tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md)|Create a new tenantCustomizedInformation object.|
|[List tenantsDetailedInformation](../api/managedtenants-managedtenant-list-tenantsdetailedinformation.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) collection|Get the tenantDetailedInformation resources from the tenantsDetailedInformation navigation property.|
|[Create tenantDetailedInformation](../api/managedtenants-managedtenant-post-tenantsdetailedinformation.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md)|Create a new tenantDetailedInformation object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md).|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|aggregatedPolicyCompliances|[microsoft.graph.managedTenants.aggregatedPolicyCompliance](../resources/managedtenants-aggregatedpolicycompliance.md) collection|**TODO: Add Description**|
|cloudPcConnections|[microsoft.graph.managedTenants.cloudPcConnection](../resources/managedtenants-cloudpcconnection.md) collection|**TODO: Add Description**|
|cloudPcDevices|[microsoft.graph.managedTenants.cloudPcDevice](../resources/managedtenants-cloudpcdevice.md) collection|**TODO: Add Description**|
|cloudPcsOverview|[microsoft.graph.managedTenants.cloudPcOverview](../resources/managedtenants-cloudpcoverview.md) collection|**TODO: Add Description**|
|conditionalAccessPolicyCoverages|[microsoft.graph.managedTenants.conditionalAccessPolicyCoverage](../resources/managedtenants-conditionalaccesspolicycoverage.md) collection|**TODO: Add Description**|
|credentialUserRegistrationsSummaries|[microsoft.graph.managedTenants.credentialUserRegistrationsSummary](../resources/managedtenants-credentialuserregistrationssummary.md) collection|**TODO: Add Description**|
|deviceCompliancePolicySettingStateSummaries|[microsoft.graph.managedTenants.deviceCompliancePolicySettingStateSummary](../resources/managedtenants-intune-devicecompliancepolicysettingstatesummary.md) collection|**TODO: Add Description**|
|managedDeviceCompliances|[microsoft.graph.managedTenants.managedDeviceCompliance](../resources/managedtenants-manageddevicecompliance.md) collection|**TODO: Add Description**|
|managedDeviceComplianceTrends|[microsoft.graph.managedTenants.managedDeviceComplianceTrend](../resources/managedtenants-manageddevicecompliancetrend.md) collection|**TODO: Add Description**|
|riskyUsers|[microsoft.graph.managedTenants.riskyUser](../resources/managedtenants-riskyuser.md) collection|**TODO: Add Description**|
|tenants|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|**TODO: Add Description**|
|tenantsCustomizedInformation|[microsoft.graph.managedTenants.tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) collection|**TODO: Add Description**|
|tenantsDetailedInformation|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) collection|**TODO: Add Description**|
|windowsDeviceMalwareStates|[microsoft.graph.managedTenants.windowsDeviceMalwareState](../resources/managedtenants-intune-windowsdevicemalwarestate.md) collection|**TODO: Add Description**|
|windowsProtectionStates|[microsoft.graph.managedTenants.windowsProtectionState](../resources/managedtenants-intune-windowsprotectionstate.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.managedTenant",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.managedTenant",
  "id": "String (identifier)"
}
```

