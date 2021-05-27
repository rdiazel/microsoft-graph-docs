---
title: "riskyUser resource type"
description: "Represents Azure AD users who are at risk across managed tenants. Azure AD continually evaluates user risk based on various signals and machine learning."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# riskyUser resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents Azure AD users who are at risk across managed tenants. Azure AD continually evaluates user risk based on various signals and machine learning.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List riskyUsers](../api/managedTenants-riskyuser-list.md)|[riskyUser](../resources/managedTenants-riskyuser.md) collection|Get a list of the [riskyUser](../resources/managedTenants-riskyuser.md) objects and their properties.|
|[Get riskyUser](../api/managedTenants-riskyuser-get.md)|[riskyUser](../resources/managedTenants-riskyuser.md)|Read the properties and relationships of a [riskyUser](../resources/managedTenants-riskyuser.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier for this entity.|
|isDeleted|Boolean|A flag indicating whether the user has been deleted.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|riskDetail|riskDetail|Details of the detected risk. Possible values are: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `hidden`, `adminConfirmedUserCompromised`, `unknownFutureValue`.|
|riskLastUpdatedDateTime|DateTimeOffset|The date and time that the risky user was last updated.|
|riskLevel|riskLevel|Level of the detected risky user. Possible values are: `low`, `medium`, `high`, `hidden`, `none`, `unknownFutureValue`.|
|riskState|riskState|State of the user's risk. Possible values are: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The Azure Active Directory tenant identifier for the managed tenant.|
|userDisplayName|String|Display name for the Azure AD user.|
|userId|String|Unique identifier for the Azure AD user.|
|userPrincipalName|String|The user principal name for the Azure AD user.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.riskyUser",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.riskyUser",
  "id": "String (identifier)",
  "userId": "String",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "userDisplayName": "String",
  "userPrincipalName": "String",
  "riskState": "String",
  "riskLevel": "String",
  "riskDetail": "String",
  "isDeleted": "Boolean",
  "riskLastUpdatedDateTime": "String (timestamp)",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
