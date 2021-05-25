---
title: "tenantGroup resource type"
description: "**TODO: Add Description**"
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenantGroup resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/managedtenants-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List tenantGroups](../api/managedtenants-tenantgroup-list.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|Get a list of the [tenantGroup](../resources/managedtenants-tenantgroup.md) objects and their properties.|
|[Create tenantGroup](../api/managedtenants-tenantgroup-create.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md)|Create a new [tenantGroup](../resources/managedtenants-tenantgroup.md) object.|
|[Get tenantGroup](../api/managedtenants-tenantgroup-get.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md)|Read the properties and relationships of a [tenantGroup](../resources/managedtenants-tenantgroup.md) object.|
|[Update tenantGroup](../api/managedtenants-tenantgroup-update.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md)|Update the properties of a [tenantGroup](../resources/managedtenants-tenantgroup.md) object.|
|[Delete tenantGroup](../api/managedtenants-tenantgroup-delete.md)|None|Deletes a [tenantGroup](../resources/managedtenants-tenantgroup.md) object.|
|[tenantSearch](../api/managedtenants-tenantgroup-tenantsearch.md)|[microsoft.graph.managedTenants.tenantGroup](../resources/managedtenants-tenantgroup.md) collection|**TODO: Add Description**|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|allTenantsIncluded|Boolean|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md).|
|managementActions|[microsoft.graph.managedTenants.managementActionInfo](../resources/managedtenants-managementactioninfo.md) collection|**TODO: Add Description**|
|managementIntents|[microsoft.graph.managedTenants.managementIntentInfo](../resources/managedtenants-managementintentinfo.md) collection|**TODO: Add Description**|
|tenantIds|String collection|**TODO: Add Description**|

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

