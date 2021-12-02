---
title: "passwordValidationInformation resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# passwordValidationInformation resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties
|Property|Type|Description|
|:---|:---|:---|
|isValid|Boolean|**TODO: Add Description**|
|validationResults|[validationResult](../resources/validationresult.md) collection|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.passwordValidationInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.passwordValidationInformation",
  "isValid": "Boolean",
  "validationResults": [
    {
      "@odata.type": "microsoft.graph.validationResult"
    }
  ]
}
```
