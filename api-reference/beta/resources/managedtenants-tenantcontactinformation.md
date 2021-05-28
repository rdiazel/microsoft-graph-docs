---
title: "tenantContactInformation resource type"
description: "Represents contact information for a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# tenantContactInformation resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents contact information for a managed tenant.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|email|String|The email address for a contact of the managed tenant.|
|name|String|The name for a contact of the managed tenant.|
|notes|String|Notes for a contact of the managed tenant.|
|phone|String|The phone number for a contact of the managed tenant.|
|title|String|The title for a contact of the managed tenant.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.tenantContactInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantContactInformation",
  "name": "String",
  "title": "String",
  "email": "String",
  "phone": "String",
  "notes": "String"
}
```
