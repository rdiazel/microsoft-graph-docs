---
title: "managedTenant resource type"
description: "**TODO: Add Description**"
author: "isaiahwilliams"
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
|[List managementActions](../api/managedtenants-managedtenant-list-managementactions.md)|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md) collection|Get the managementAction resources from the managementActions navigation property.|
|[Create managementAction](../api/managedtenants-managedtenant-post-managementactions.md)|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md)|Create a new managementAction object.|
|[List managementActionTenantDeploymentStatuses](../api/managedtenants-managedtenant-list-managementactiontenantdeploymentstatuses.md)|[microsoft.graph.managedTenants.managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) collection|Get the managementActionTenantDeploymentStatus resources from the managementActionTenantDeploymentStatuses navigation property.|
|[Create managementActionTenantDeploymentStatus](../api/managedtenants-managedtenant-post-managementactiontenantdeploymentstatuses.md)|[microsoft.graph.managedTenants.managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md)|Create a new managementActionTenantDeploymentStatus object.|
|[List managementIntents](../api/managedtenants-managedtenant-list-managementintents.md)|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md) collection|Get the managementIntent resources from the managementIntents navigation property.|
|[Create managementIntent](../api/managedtenants-managedtenant-post-managementintents.md)|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md)|Create a new managementIntent object.|
|[List managementTemplates](../api/managedtenants-managedtenant-list-managementtemplates.md)|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md) collection|Get the managementTemplate resources from the managementTemplates navigation property.|
|[Create managementTemplate](../api/managedtenants-managedtenant-post-managementtemplates.md)|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md)|Create a new managementTemplate object.|
|[List tenantGroups](../api/managedtenants-managedtenant-list-tenantgroups.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|Get the tenantGroup resources from the tenantGroups navigation property.|
|[Create tenantGroup](../api/managedtenants-managedtenant-post-tenantgroups.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md)|Create a new tenantGroup object.|

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
|managementActions|[microsoft.graph.managedTenants.managementAction](../resources/managedtenants-managementaction.md) collection|**TODO: Add Description**|
|managementActionTenantDeploymentStatuses|[microsoft.graph.managedTenants.managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) collection|**TODO: Add Description**|
|managementIntents|[microsoft.graph.managedTenants.managementIntent](../resources/managedtenants-managementintent.md) collection|**TODO: Add Description**|
|managementTemplates|[microsoft.graph.managedTenants.managementTemplate](../resources/managedtenants-managementtemplate.md) collection|**TODO: Add Description**|
|riskyUsers|[microsoft.graph.managedTenants.riskyUser](../resources/managedtenants-riskyuser.md) collection|**TODO: Add Description**|
|tenantGroups|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|**TODO: Add Description**|
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

