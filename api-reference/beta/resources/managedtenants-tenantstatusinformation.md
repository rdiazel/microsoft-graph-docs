---
title: "tenantStatusInformation resource type"
description: "Represents the information regarding onboarding status of the managed tenant."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# tenantStatusInformation resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the information regarding onboarding status of the managed tenant.

## Properties

|Property|Type|Description|
|:---|:---|:---|
|delegatedPrivilegeStatus|delegatedPrivilegeStatus|The status of the delegated admin privileges relationship that exists with the managed tenant. Possible values are: `none`, `delegatedAdminPrivileges`, `unknownFutureValue`.|
|lastDelegatedPrivilegeRefreshDateTime|DateTimeOffset|The date and time the delegated admin privilege relationship information was last refreshed.|
|offboardedByUserId|String|The identifier of the user that performed the off boarding action. If this is empty the managed tenant has either not been off boarded or the action was performed automatically.|
|offboardedDateTime|DateTimeOffset|The date and time the managed tenant was off boarded.|
|onboardedByUserId|String|The identifier of the user that on boarded the managed tenant. If this is empty the platform automatically on boarded the managed tenant.|
|onboardedDateTime|DateTimeOffset|The date and time the managed tenant was on boarded.|
|onboardingStatus|tenantOnboardingStatus|The on boarding status for the managed to the management platform. Possible values are: `ineligible`, `inProcess`, `active`, `inactive`, `unknownFutureValue`.|
|workloadStatuses|[microsoft.graph.managedTenants.workloadStatus](../resources/managedtenants-workloadstatus.md) collection|The on boarding information for each Microsoft 365 service currently supported by the management platform.|

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
