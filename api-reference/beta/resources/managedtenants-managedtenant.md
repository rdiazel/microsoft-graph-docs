---
title: "managedTenant resource type"
description: "The managedTenant resource represents a container for the actions and resources that are managed by Microsoft 365 Lighthouse."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# managedTenant resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The managedTenant resource represents a container for the actions and resources that are managed by Microsoft 365 Lighthouse.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List managementActions](../api/managedtenants-managedtenant-list-managementactions.md)|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md) collection|Get the managementAction resources from the managementActions navigation property.|
|[List managementActionTenantDeploymentStatuses](../api/managedtenants-managedtenant-list-managementactiontenantdeploymentstatuses.md)|[microsoft.graph.managedTenants.managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) collection|Get the managementActionTenantDeploymentStatus resources from the managementActionTenantDeploymentStatuses navigation property.|
|[List managementIntents](../api/managedtenants-managedtenant-list-managementintents.md)|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md) collection|Get the managementIntent resources from the managementIntents navigation property.|
|[List managementTemplates](../api/managedtenants-managedtenant-list-managementtemplates.md)|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md) collection|Get the managementTemplate resources from the managementTemplates navigation property.|
|[List tenantGroups](../api/managedtenants-managedtenant-list-tenantgroups.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|Get the tenantGroup resources from the tenantGroups navigation property.|
|[List tenantTags](../api/managedtenants-managedtenant-list-tenanttags.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md) collection|Get the tenantTag resources from the tenantTags navigation property.|
|[Create tenantTag](../api/managedtenants-managedtenant-post-tenanttags.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md)|Create a new tenantTag object.|
|[List tenants](../api/managedtenants-managedtenant-list-tenants.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|Get the tenant resources from the tenants navigation property.|
|[List tenantsCustomizedInformation](../api/managedtenants-managedtenant-list-tenantscustomizedinformation.md)|[microsoft.graph.managedTenants.tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) collection|Get the tenantCustomizedInformation resources from the tenantsCustomizedInformation navigation property.|
|[List tenantsDetailedInformation](../api/managedtenants-managedtenant-list-tenantsdetailedinformation.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) collection|Get the tenantDetailedInformation resources from the tenantsDetailedInformation navigation property.|
|[List tenantTags](../api/managedtenants-managedtenant-list-tenanttags.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md) collection|Get the tenantTag resources from the tenantTags navigation property.|
|[Create tenantTag](../api/managedtenants-managedtenant-post-tenanttags.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md)|Create a new tenantTag object.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description**.|

## Relationships

|Relationship|Type|Description|
|:---|:---|:---|
|aggregatedPolicyCompliances|[microsoft.graph.managedTenants.aggregatedPolicyCompliance](../resources/managedtenants-aggregatedpolicycompliance.md) collection|The aggregated device compliance details for each managed tenant.|
|cloudPcConnections|[microsoft.graph.managedTenants.cloudPcConnection](../resources/managedtenants-cloudpcconnection.md) collection|The Cloud PC connections for each managed tenant.|
|cloudPcDevices|[microsoft.graph.managedTenants.cloudPcDevice](../resources/managedtenants-cloudpcdevice.md) collection|The Cloud PC devices for each managed tenant.|
|cloudPcsOverview|[microsoft.graph.managedTenants.cloudPcOverview](../resources/managedtenants-cloudpcoverview.md) collection|The Cloud PC overview details for each managed tenant.|
|conditionalAccessPolicyCoverages|[microsoft.graph.managedTenants.conditionalAccessPolicyCoverage](../resources/managedtenants-conditionalaccesspolicycoverage.md) collection|The conditional access policy coverage details for each managed tenant.|
|credentialUserRegistrationsSummaries|[microsoft.graph.managedTenants.credentialUserRegistrationsSummary](../resources/managedtenants-credentialuserregistrationssummary.md) collection|The credential user registration summaries for each managed tenant.|
|deviceCompliancePolicySettingStateSummaries|[microsoft.graph.managedTenants.deviceCompliancePolicySettingStateSummary](../resources/managedtenants-devicecompliancepolicysettingstatesummary.md) collection|The setting state summary for device compliance policies in each managed tenant.|
|managedDeviceCompliances|[microsoft.graph.managedTenants.managedDeviceCompliance](../resources/managedtenants-manageddevicecompliance.md) collection|The managed device compliance details for each managed tenant.|
|managedDeviceComplianceTrends|[microsoft.graph.managedTenants.managedDeviceComplianceTrend](../resources/managedtenants-manageddevicecompliancetrend.md) collection|The device compliance trends for each managed tenant.|
|managementActions|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md) collection|The available management actions for each managed tenant.|
|managementActionTenantDeploymentStatuses|[microsoft.graph.managedTenants.managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) collection|The tenant level deployment status related to the available management actions for each managed tenants.|
|managementIntents|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md) collection|The available management intents for each managed tenant.|
|managementTemplates|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md) collection|The available management templates for each managed tenant.|
|riskyUsers|[microsoft.graph.managedTenants.riskyUser](../resources/managedtenants-riskyuser.md) collection|The collection of users who have been flagged for risk in each managed tenant.|
|tenantGroups|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|The available tenant groups for each managed tenant.|
|tenants|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|The collection of tenant that have a relationship with the managing entity.|
|tenantsCustomizedInformation|[microsoft.graph.managedTenants.tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) collection|The customized information managed by the managing entity for each managed tenant.|
|tenantsDetailedInformation|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) collection|The detailed information for each managed tenant.|
|tenantTags|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md) collection|Tags that can be assigned to managed tenant.|
|windowsDeviceMalwareStates|[microsoft.graph.managedTenants.windowsDeviceMalwareState](../resources/managedtenants-windowsdevicemalwarestate.md) collection|The state of detected malware on devices running Windows for each managed tenant.|
|windowsProtectionStates|[microsoft.graph.managedTenants.windowsProtectionState](../resources/managedtenants-windowsprotectionstate.md) collection|The protection state information available on devices running Windows for each managed tenant.|

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
