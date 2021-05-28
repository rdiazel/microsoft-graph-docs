---
title: "tenantGroup resource type"
description: "Represents a logical group of managed tenants."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# tenantGroup resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a logical group of managed tenants.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List tenantGroups](../api/managedtenants-tenantgroup-list.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|Get a list of the [tenantGroup](../resources/managedtenants-tenantgroup.md) objects and their properties.|
|[Get tenantGroup](../api/managedtenants-tenantgroup-get.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md)|Read the properties and relationships of a [tenantGroup](../resources/managedtenants-tenantgroup.md) object.|
|[tenantSearch](../api/managedtenants-tenantgroup-tenantsearch.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|Searches for all tenant groups that contain a specific managed tenant identifier.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|allTenantsIncluded|Boolean|A flag indicating whether all managed tenants are included in the tenant group.|
|displayName|String|The display name of the tenant group.|
|id|String|The unique identifier of the tenant group.|
|managementActions|[microsoft.graph.managedTenants.managementActionInfo](../resources/managedtenants-managementactioninfo.md) collection|A collection of management actions associated with the tenant group.|
|managementIntents|[microsoft.graph.managedTenants.managementIntentInfo](../resources/managedtenants-managementintentinfo.md) collection|A collection of management actions associated with the tenant group.|
|tenantIds|String collection|A collection of managed tenant identifier that are included in the tenant group.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.tenantGroup",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantGroup",
  "id": "String (identifier)",
  "displayName": "String",
  "allTenantsIncluded": "Boolean",
  "tenantIds": [
    "String"
  ],
  "managementIntents": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementIntentInfo"
    }
  ],
  "managementActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementActionInfo"
    }
  ]
}
```
