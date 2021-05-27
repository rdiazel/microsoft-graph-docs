---
title: "credentialUserRegistrationsSummary resource type"
description: "Represents a summary of the number of users across managed tenants that have multi-factor authentication enabled."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft365-lighthouse"
doc_type: resourcePageType
---

# credentialUserRegistrationsSummary resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a summary of the number of users across managed tenants that have multi-factor authentication enabled.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List credentialUserRegistrationsSummaries](../api/managedTenants-credentialuserregistrationssummary-list.md)|[credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md) collection|Get a list of the [credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md) objects and their properties.|
|[Get credentialUserRegistrationsSummary](../api/managedTenants-credentialuserregistrationssummary-get.md)|[credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md)|Read the properties and relationships of a [credentialUserRegistrationsSummary](../resources/managedTenants-credentialuserregistrationssummary.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier for this entity.|
|lastRefreshedDateTime|DateTimeOffset|The last time the data for this entity was updated.|
|mfaAndSsprCapableUserCount|Int32|Number of users that are able to perform self-service password resets or multi-factor authentication.|
|mfaConditionalAccessPolicyState|String|Specifies the state of the conditionalAccessPolicy object. Possible values are: `enabled`, `disabled`, `enabledForReportingButNotEnforced`.|
|mfaRegisteredUserCount|Int32|Number of users that are registered for multi-factor authentication.|
|securityDefaultsEnabled|Boolean|A flag that indicates whether Identity Security Defaults is enabled.|
|ssprEnabledUserCount|Int32|Number of users that are enabled for self-service password reset.|
|ssprRegisteredUserCount|Int32|Number of users that have registered for self-service password reset.|
|tenantDisplayName|String|Display name for the managed tenant.|
|tenantId|String|The Azure Active Directory identifier for the managed tenant.|
|totalUserCount|Int32|Total number of accounts in the managed tenant.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.credentialUserRegistrationsSummary",
  "openType": true
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.credentialUserRegistrationsSummary",
  "id": "String (identifier)",
  "tenantId": "String",
  "tenantDisplayName": "String",
  "mfaAndSsprCapableUserCount": "Integer",
  "ssprEnabledUserCount": "Integer",
  "mfaRegisteredUserCount": "Integer",
  "ssprRegisteredUserCount": "Integer",
  "totalUserCount": "Integer",
  "securityDefaultsEnabled": "Boolean",
  "mfaConditionalAccessPolicyState": "String",
  "lastRefreshedDateTime": "String (timestamp)"
}
```
