---
title: "Create tenantReference"
description: "Create a new tenantReference object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create tenantReference
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new tenantReference object.

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
POST /directory/outboundSharedUserProfiles/{outboundSharedUserProfileId}/tenants
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [tenantReference](../resources/tenantreference.md) object.

You can specify the following properties when creating a **tenantReference**.

|Property|Type|Description|
|:---|:---|:---|
|deletedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [directoryObject](../resources/directoryobject.md). Optional.|
|tenantId|String|**TODO: Add Description** Required.|



## Response

If successful, this method returns a `201 Created` response code and a [tenantReference](../resources/tenantreference.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_tenantreference_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/directory/outboundSharedUserProfiles/{outboundSharedUserProfileId}/tenants
Content-Type: application/json
Content-length: 138

{
  "@odata.type": "#Microsoft.DirectoryServices.tenantReference",
  "deletedDateTime": "String (timestamp)",
  "tenantId": "String"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Microsoft.DirectoryServices.tenantReference"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#Microsoft.DirectoryServices.tenantReference",
  "id": "bc7f83fc-83fc-bc7f-fc83-7fbcfc837fbc",
  "deletedDateTime": "String (timestamp)",
  "tenantId": "String"
}
```
