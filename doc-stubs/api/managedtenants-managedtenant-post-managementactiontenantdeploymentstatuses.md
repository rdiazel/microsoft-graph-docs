---
title: "Create managementActionTenantDeploymentStatus"
description: "Create a new managementActionTenantDeploymentStatus object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create managementActionTenantDeploymentStatus
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new managementActionTenantDeploymentStatus object.

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
POST /tenantRelationships/managedTenants/managementActionTenantDeploymentStatuses
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) object.

The following table shows the properties that are required when you create the [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|tenantGroupId|String|**TODO: Add Description**|
|tenantId|String|**TODO: Add Description**|
|statuses|[microsoft.graph.managedTenants.managementActionDeploymentStatus](../resources/managedtenants-managementactiondeploymentstatus.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [managementActionTenantDeploymentStatus](../resources/managedtenants-managementactiontenantdeploymentstatus.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_managementactiontenantdeploymentstatus_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementActionTenantDeploymentStatuses
Content-Type: application/json
Content-length: 275

{
  "@odata.type": "#microsoft.graph.managedTenants.managementActionTenantDeploymentStatus",
  "tenantGroupId": "String",
  "tenantId": "String",
  "statuses": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementActionDeploymentStatus"
    }
  ]
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.managementActionTenantDeploymentStatus"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.managementActionTenantDeploymentStatus",
  "id": "acc7b87a-b87a-acc7-7ab8-c7ac7ab8c7ac",
  "tenantGroupId": "String",
  "tenantId": "String",
  "statuses": [
    {
      "@odata.type": "microsoft.graph.managedTenants.managementActionDeploymentStatus"
    }
  ]
}
```

