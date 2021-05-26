---
title: "Create tenantTag"
description: "Create a new tenantTag object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create tenantTag
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new tenantTag object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ManagedTenants.WriteRead.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /tenantRelationships/managedTenants/tenantTags
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [tenantTag](../resources/managedtenants-tenanttag.md) object.

The following table shows the properties that are required when you create the [tenantTag](../resources/managedtenants-tenanttag.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier of the tenant tag. Inherited from [entity](../resources/managedtenants-entity.md)|
|displayName|String|The display name of the tenant tag.|
|description|String|The description of the tenant tag.|
|createdByUserId|String|The identifier of the user that created the tenant tag.|
|modifiedByUserId|String|The identifier of the user that modified the tenant tag.|
|managedTenants|[microsoft.graph.managedTenants.managedTenantInfo](../resources/managedtenants-managedtenantinfo.md) collection|A collection of managed tenant information associated with the tenant tag.|
|lastModifiedDateTime|DateTimeOffset|The date and time the tenant tag was last modified.|
|deletedDateTime|DateTimeOffset|The date and time the tenant tag was deleted.|

## Response

If successful, this method returns a `201 Created` response code and a [tenantTag](../resources/managedtenants-tenanttag.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_tenanttag_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/tenantRelationships/managedTenants/tenantTags
Content-Type: application/json
Content-length: 347

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantTag",
  "displayName": "String",
  "description": "String",
  "createdByUserId": "String",
  "modifiedByUserId": "String",
  "managedTenants": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managedTenantInfo"
    }
  ],
  "deletedDateTime": "String (timestamp)"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.tenantTag"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantTag",
  "id": "9046c8c9-c8c9-9046-c9c8-4690c9c84690",
  "displayName": "String",
  "description": "String",
  "createdByUserId": "String",
  "modifiedByUserId": "String",
  "managedTenants": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managedTenantInfo"
    }
  ],
  "lastModifiedDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)"
}
```
