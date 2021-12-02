---
title: "List excludes"
description: "Get the permissionGrantConditionSet resources from the excludes navigation property."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List excludes
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the permissionGrantConditionSet resources from the excludes navigation property.

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
GET /permissionGrantPolicy/excludes
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [permissionGrantConditionSet](../resources/permissiongrantconditionset.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_permissiongrantconditionset"
}
-->
``` http
GET https://graph.microsoft.com/beta/permissionGrantPolicy/excludes
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(Microsoft.DirectoryServices.permissionGrantConditionSet)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#Microsoft.DirectoryServices.permissionGrantConditionSet",
      "id": "0be3542d-542d-0be3-2d54-e30b2d54e30b",
      "permissionClassification": "String",
      "permissionType": "String",
      "resourceApplication": "String",
      "permissions": [
        "String"
      ],
      "clientApplicationIds": [
        "String"
      ],
      "clientApplicationTenantIds": [
        "String"
      ],
      "clientApplicationPublisherIds": [
        "String"
      ],
      "clientApplicationsFromVerifiedPublisherOnly": "Boolean",
      "certifiedClientApplicationsOnly": "Boolean"
    }
  ]
}
```
