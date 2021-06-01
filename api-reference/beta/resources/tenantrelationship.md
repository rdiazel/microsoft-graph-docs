---
title: tenantRelationship resource type
description: 'Container for entities and operations relating to tenant relationships.'
author: isaiahwilliams
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# tenantRelationship resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

## Relationships

| Relationship   | Type                                             | Description |
| :------------- | :----------------------------------------------- | :---------- |
| managedTenants | [managedTenant](managedtenants-managedtenant.md) |             |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.tenantRelationship",
  "baseType": "microsoft.graph.entity",
  "openType": False
}
-->

```json
{
  "@odata.type": "#microsoft.graph.tenantRelationship"
}
```
