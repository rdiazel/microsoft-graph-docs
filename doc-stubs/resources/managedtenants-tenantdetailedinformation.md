---
title: "tenantDetailedInformation resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# tenantDetailedInformation resource type

Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [entity](../resources/managedtenants-entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List tenantDetailedInformations](../api/managedtenants-tenantdetailedinformation-list.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) collection|Get a list of the [tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) objects and their properties.|
|[Create tenantDetailedInformation](../api/managedtenants-tenantdetailedinformation-create.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md)|Create a new [tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) object.|
|[Get tenantDetailedInformation](../api/managedtenants-tenantdetailedinformation-get.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md)|Read the properties and relationships of a [tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) object.|
|[Update tenantDetailedInformation](../api/managedtenants-tenantdetailedinformation-update.md)|[microsoft.graph.managedTenants.tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md)|Update the properties of a [tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) object.|
|[Delete tenantDetailedInformation](../api/managedtenants-tenantdetailedinformation-delete.md)|None|Deletes a [tenantDetailedInformation](../resources/managedtenants-tenantdetailedinformation.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|city|String|**TODO: Add Description**|
|countryCode|String|**TODO: Add Description**|
|countryName|String|**TODO: Add Description**|
|defaultDomainName|String|**TODO: Add Description**|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/managedtenants-entity.md).|
|industryName|String|**TODO: Add Description**|
|region|String|**TODO: Add Description**|
|segmentName|String|**TODO: Add Description**|
|tenantId|String|**TODO: Add Description**|
|verticalName|String|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedTenants.tenantDetailedInformation",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedTenants.tenantDetailedInformation",
  "id": "String (identifier)",
  "tenantId": "String",
  "displayName": "String",
  "defaultDomainName": "String",
  "countryName": "String",
  "countryCode": "String",
  "city": "String",
  "region": "String",
  "verticalName": "String",
  "industryName": "String",
  "segmentName": "String"
}
```

