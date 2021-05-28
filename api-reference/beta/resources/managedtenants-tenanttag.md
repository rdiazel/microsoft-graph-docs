---
title: "tenantTag resource type"
description: "Represent a tag related to a managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# tenantTag resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represent a tag associated with a managed tenant.

## Methods

|Method|Return type|Description|
|:---|:---|:---|
|[List tenantTags](../api/managedtenants-tenanttag-list.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md) collection|Get a list of the [tenantTag](../resources/managedtenants-tenanttag.md) objects and their properties.|
|[Create tenantTag](../api/managedtenants-tenanttag-create.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md)|Create a new [tenantTag](../resources/managedtenants-tenanttag.md) object.|
|[Get tenantTag](../api/managedtenants-tenanttag-get.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md)|Read the properties and relationships of a [tenantTag](../resources/managedtenants-tenanttag.md) object.|
|[Update tenantTag](../api/managedtenants-tenanttag-update.md)|[microsoft.graph.managedTenants.tenantTag](../resources/managedtenants-tenanttag.md)|Update the properties of a [tenantTag](../resources/managedtenants-tenanttag.md) object.|
|[Delete tenantTag](../api/managedtenants-tenanttag-delete.md)|None|Deletes a [tenantTag](../resources/managedtenants-tenanttag.md) object.|

## Properties

|Property|Type|Description|
|:---|:---|:---|
|createdByUserId|String|The Azure Active Directory user identifier of the user that created the tenant tag.|
|createdDateTime|DateTimeOffset|The date and time the tenant tag was created.|
|deletedDateTime|DateTimeOffset|The date and time the tenant tag was deleted.|
|description|String|The description of the tenant tag.|
|displayName|String|The display name of the tenant tag.|
|id|String|The unique identifier of the tenant tag.|
|lastActionByUserId|String|The Azure Active Directory user identifier of the user that acted on the tenant last.|
|lastActionDateTime|DateTimeOffset|The date and time when the last action against the tenant tag.|
|tenantIds|String collection|A collection of Azure Active Directory tenant identifiers of managed tenants associated with the tenant tag.|

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.tenantTag",
  "baseType": "microsoft.graph.entity",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantTag",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdByUserId": "String",
  "lastActionByUserId": "String",
  "tenantIds": [
    "String"
  ],
  "lastActionDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)"
}
```
