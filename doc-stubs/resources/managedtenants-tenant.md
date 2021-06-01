---
title: "tenant resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenant resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/managedtenants-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List tenants](../api/managedtenants-tenant-list.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md) collection|Get a list of the [tenant](../resources/managedtenants-tenant.md) objects and their properties.|
|[Create tenant](../api/managedtenants-tenant-create.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Create a new [tenant](../resources/managedtenants-tenant.md) object.|
|[Get tenant](../api/managedtenants-tenant-get.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Read the properties and relationships of a [tenant](../resources/managedtenants-tenant.md) object.|
|[Update tenant](../api/managedtenants-tenant-update.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|Update the properties of a [tenant](../resources/managedtenants-tenant.md) object.|
|[Delete tenant](../api/managedtenants-tenant-delete.md)|None|Deletes a [tenant](../resources/managedtenants-tenant.md) object.|
|[offboardTenant](../api/managedtenants-tenant-offboardtenant.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|**TODO: Add Description**|
|[resetTenantOnboardingStatus](../api/managedtenants-tenant-resettenantonboardingstatus.md)|[microsoft.graph.managedTenants.tenant](../resources/managedtenants-tenant.md)|**TODO: Add Description**|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|contract|[microsoft.graph.managedTenants.tenantContract](../resources/managedtenants-tenantcontract.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md).|
|lastUpdatedDateTime|DateTimeOffset|**TODO: Add Description**|
|tenantId|String|**TODO: Add Description**|
|tenantStatusInformation|[microsoft.graph.managedTenants.tenantStatusInformation](../resources/managedtenants-tenantstatusinformation.md)|**TODO: Add Description**|

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

