---
title: "Create tenant"
description: "Create a new tenant object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create tenant
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new [tenant](../resources/managedtenants-tenant.md) object.

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
POST /tenantRelationships/managedTenants/tenants
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [tenant](../resources/managedtenants-tenant.md) object.

The following table shows the properties that are required when you create the [tenant](../resources/managedtenants-tenant.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|tenantId|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|contract|[microsoft.graph.managedTenants.tenantContract](../resources/managedtenants-tenantcontract.md)|**TODO: Add Description**|
|tenantStatusInformation|[microsoft.graph.managedTenants.tenantStatusInformation](../resources/managedtenants-tenantstatusinformation.md)|**TODO: Add Description**|
|lastUpdatedDateTime|DateTimeOffset|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [tenant](../resources/managedtenants-tenant.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_tenant_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/tenantRelationships/managedTenants/tenants
Content-Type: application/json
Content-length: 370

{
  "@odata.type": "#microsoft.graph.managedTenants.tenant",
  "tenantId": "String",
  "displayName": "String",
  "contract": {
    "@odata.type": "microsoft.graph.managedTenants.tenantContract"
  },
  "tenantStatusInformation": {
    "@odata.type": "microsoft.graph.managedTenants.tenantStatusInformation"
  },
  "lastUpdatedDateTime": "String (timestamp)"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.tenant"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.tenant",
  "id": "36fab3ad-b3ad-36fa-adb3-fa36adb3fa36",
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

