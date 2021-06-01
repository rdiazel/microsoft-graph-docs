---
title: "tenantStatusInformation resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenantStatusInformation resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|delegatedPrivilegeStatus|delegatedPrivilegeStatus|**TODO: Add Description**. Possible values are: `none`, `delegatedAdminPrivileges`, `unknownFutureValue`.|
|lastDelegatedPrivilegeRefreshDateTime|DateTimeOffset|**TODO: Add Description**|
|offboardedByUserId|String|**TODO: Add Description**|
|offboardedDateTime|DateTimeOffset|**TODO: Add Description**|
|onboardedByUserId|String|**TODO: Add Description**|
|onboardedDateTime|DateTimeOffset|**TODO: Add Description**|
|onboardingStatus|tenantOnboardingStatus|**TODO: Add Description**. Possible values are: `ineligible`, `inProcess`, `active`, `inactive`, `unknownFutureValue`.|
|workloadStatuses|[microsoft.graph.managedTenants.workloadStatus](../resources/managedtenants-workloadstatus.md) collection|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedTenants.tenantStatusInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantStatusInformation",
  "onboardingStatus": "String",
  "onboardedDateTime": "String (timestamp)",
  "onboardedByUserId": "String",
  "offboardedDateTime": "String (timestamp)",
  "offboardedByUserId": "String",
  "delegatedPrivilegeStatus": "String",
  "lastDelegatedPrivilegeRefreshDateTime": "String (timestamp)",
  "workloadStatuses": [
    {
      "@odata.type": "microsoft.graph.managedTenants.workloadStatus"
    }
  ]
}
```

