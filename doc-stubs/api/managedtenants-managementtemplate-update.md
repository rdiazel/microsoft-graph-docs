---
title: "Update managementTemplate"
description: "Update the properties of a managementTemplate object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update managementTemplate
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [managementTemplate](../resources/managedtenants-managementtemplate.md) object.

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
PATCH /tenantRelationships/managedTenants/managementTemplates/{managementTemplateId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [managementTemplate](../resources/managedtenants-managementtemplate.md) object.

The following table shows the properties that are required when you update the [managementTemplate](../resources/managedtenants-managementtemplate.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md)|
|displayName|String|**TODO: Add Description**|
|description|String|**TODO: Add Description**|
|category|managementCategory|**TODO: Add Description**. Possible values are: `devices`, `identity`, `custom`, `unknownFutureValue`.|
|version|Int32|**TODO: Add Description**|
|parameters|[microsoft.graph.managedTenants.templateParameter](../resources/managedtenants-templateparameter.md) collection|**TODO: Add Description**|
|workloadActions|[microsoft.graph.managedTenants.workloadAction](../resources/managedtenants-workloadaction.md) collection|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [managementTemplate](../resources/managedtenants-managementtemplate.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_managementtemplate"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/tenantRelationships/managedTenants/managementTemplates/{managementTemplateId}
Content-Type: application/json
Content-length: 407

{
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplate",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "version": "Integer",
  "parameters": [
    {
      "@odata.type": "microsoft.graph.managedTenants.templateParameter"
    }
  ],
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
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
  "@odata.type": "#microsoft.graph.managedTenants.managementTemplate",
  "id": "3a4de886-e886-3a4d-86e8-4d3a86e84d3a",
  "displayName": "String",
  "description": "String",
  "category": "String",
  "version": "Integer",
  "parameters": [
    {
      "@odata.type": "microsoft.graph.managedTenants.templateParameter"
    }
  ],
  "workloadActions": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadAction"
    }
  ]
}
```

