---
title: "tenant resource type"
description: "Represent a tenant that has a relationship with the managing entity."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenant resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represent a tenant that has a relationship with the managing entity.

Inherits from [entity](../resources/managedtenants-entity.md).

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List tenants](../api/managedtenants-tenant-list.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|Get a list of the [tenant](../resources/managedtenants-tenant.md) objects and their properties.|
|[Get tenant](../api/managedtenants-tenant-get.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Read the properties and relationships of a [tenant](../resources/managedtenants-tenant.md) object.|
|[offboardTenant](../api/managedtenants-tenant-offboardtenant.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Off boards a managed tenant from the management platform. The platform will not add the managed tenant back after this operation has been performed.|
|[resetTenantOnboardingStatus](../api/managedtenants-tenant-resettenantonboardingstatus.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Resets the onboarding status for a managed tenant, so the platform will attempt to enroll the tenant for management.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|contract|[microsoft.graph.managedTenants.tenantContract](../resources/managedtenants-tenantcontract.md)|The tenant contract that exists with the managed tenant.|
|createdDateTime|DateTimeOffset|The date and time when the managed tenant was created.|
|displayName|String|The display name of the managed tenant.|
|id|String|The Azure Active Directory tenant identifier of the managed tenant. Inherited from [entity](../resources/managedtenants-entity.md).|
|lastUpdatedDateTime|DateTimeOffset|The date and time the managed tenant was last updated.|
|tenantId|String|The Azure Active Directory tenant identifier of the managed tenant.|
|tenantStatusInformation|[microsoft.graph.managedTenants.tenantStatusInformation](../resources/managedtenants-tenantstatusinformation.md)|The status information of the managed tenant.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.tenant",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenant",
  "id": "String (identifier)",
  "tenantId": "String",
  "displayName": "String",
  "contract": {
    "@odata.type": "microsoft.graph.managedTenants.tenantContract"
  },
  "tenantStatusInformation": {
    "@odata.type": "microsoft.graph.managedTenants.tenantStatusInformation"
  },
  "lastUpdatedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)"
}
```
