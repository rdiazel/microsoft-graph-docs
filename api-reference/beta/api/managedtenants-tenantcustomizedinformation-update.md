---
title: "Update tenantCustomizedInformation"
description: "Update the properties of a tenantCustomizedInformation object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: apiPageType
---

# Update tenantCustomizedInformation
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ManagedTenants.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /tenantRelationships/managedTenants/tenantsCustomizedInformation/{tenantCustomizedInformationId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) object.

The following table shows the properties that are required when you update the [tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The identifier of the customized information.|
|displayName|String|The display name of the managed tenant.|
|tenantId|String|The Azure Active Directory identifier for the managed tenant.|
|contacts|[microsoft.graph.managedTenants.tenantContactInformation](../resources/managedtenants-tenantcontactinformation.md) collection|A collection of contact associated with the managed tenant.|
|website|String|The website for the managed tenant.|

## Response

If successful, this method returns a `200 OK` response code and an updated [tenantCustomizedInformation](../resources/managedtenants-tenantcustomizedinformation.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_tenantcustomizedinformation"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/tenantRelationships/managedTenants/tenantsCustomizedInformation/{tenantCustomizedInformationId}
Content-Type: application/json
Content-length: 286

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantCustomizedInformation",
  "displayName": "String",
  "tenantId": "String",
  "contacts": [
    {
      "@odata.type": "microsoft.graph.managedTenants.tenantContactInformation"
    }
  ],
  "website": "String"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.tenantCustomizedInformation"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.tenantCustomizedInformation",
  "id": "686030d7-30d7-6860-d730-6068d7306068",
  "displayName": "String",
  "tenantId": "String",
  "contacts": [
    {
      "@odata.type": "microsoft.graph.managedTenants.tenantContactInformation"
    }
  ],
  "website": "String"
}
```
