---
title: "Update tenantGroup"
description: "Update the properties of a tenantGroup object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update tenantGroup
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [tenantGroup](../resources/managedtenants-tenantgroup.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /tenantRelationships/managedTenants/tenantGroups/{tenantGroupId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [tenantGroup](../resources/managedtenants-tenantgroup.md) object.

The following table shows the properties that are required when you update the [tenantGroup](../resources/managedtenants-tenantgroup.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|displayName|String|**TODO: Add Description**|
|allTenantsIncluded|Boolean|**TODO: Add Description**|
|tenantIds|String collection|**TODO: Add Description**|
|managementIntents|[microsoft.graph.managedTenants.managementIntentInfo](../resources/managedtenants-managementintentinfo.md) collection|**TODO: Add Description**|
|managementActions|[microsoft.graph.managedTenants.managementActionInfo](../resources/managedtenants-managementactioninfo.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [tenantGroup](../resources/managedtenants-tenantgroup.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_tenantgroup"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/tenantRelationships/managedTenants/tenantGroups/{tenantGroupId}
Content-Type: application/json
Content-length: 414

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantGroup",
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


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantGroup",
  "id": "c6dcf348-f348-c6dc-48f3-dcc648f3dcc6",
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

