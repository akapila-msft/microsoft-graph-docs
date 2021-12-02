---
title: "Update device"
description: "Update the properties of a device object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update device
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [device](../resources/device.md) object.

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
PATCH /devices/{devicesId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]


|Property|Type|Description|
|:---|:---|:---|
|deletedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [directoryObject](../resources/directoryobject.md). Optional.|
|accountEnabled|Boolean|**TODO: Add Description** Optional.|
|alternativeSecurityIds|[Microsoft.DirectoryServices.alternativeSecurityId](../resources/alternativesecurityid.md) collection|**TODO: Add Description** Required.|
|approximateLastSignInDateTime|DateTimeOffset|**TODO: Add Description** Optional.|
|capabilities|deviceCapabilities collection|**TODO: Add Description**. The possible values are: `rbac`, `inferredAuth`, `unknownFutureValue`. Optional.|
|compliantApplications|[Microsoft.DirectoryServices.compliantApplication](../resources/compliantapplication.md) collection|**TODO: Add Description** Optional.|
|compliantApplicationsManagementAppId|String|**TODO: Add Description** Optional.|
|complianceExpirationDateTime|DateTimeOffset|**TODO: Add Description** Optional.|
|customSecurityAttributes|[Microsoft.DirectoryServices.customSecurityAttributeValue](../resources/customsecurityattributevalue.md)|**TODO: Add Description** Optional.|
|deviceCategory|String|**TODO: Add Description** Optional.|
|deviceId|String|**TODO: Add Description** Optional.|
|deviceKeys|[Microsoft.DirectoryServices.deviceKey](../resources/devicekey.md) collection|**TODO: Add Description** Optional.|
|deviceMetadata|String|**TODO: Add Description** Optional.|
|deviceOwnership|String|**TODO: Add Description** Optional.|
|deviceSystemMetadata|[Microsoft.DirectoryServices.keyValue](../resources/keyvalue.md)|**TODO: Add Description** Optional.|
|deviceVersion|Int32|**TODO: Add Description** Optional.|
|displayName|String|**TODO: Add Description** Optional.|
|domainName|String|**TODO: Add Description** Optional.|
|enrollmentProfileName|String|**TODO: Add Description** Optional.|
|enrollmentType|String|**TODO: Add Description** Optional.|
|extensionAttributes|[Microsoft.DirectoryServices.onPremisesExtensionAttributes](../resources/onpremisesextensionattributes.md)|**TODO: Add Description** Optional.|
|exchangeActiveSyncIds|String collection|**TODO: Add Description** Optional.|
|hostnames|String collection|**TODO: Add Description** Optional.|
|isCompliant|Boolean|**TODO: Add Description** Optional.|
|isManaged|Boolean|**TODO: Add Description** Optional.|
|isManagementRestricted|Boolean|**TODO: Add Description** Optional.|
|isRooted|Boolean|**TODO: Add Description** Optional.|
|localCredentials|String|**TODO: Add Description** Optional.|
|managementType|String|**TODO: Add Description** Optional.|
|onPremisesLastSyncDateTime|DateTimeOffset|**TODO: Add Description** Optional.|
|onPremisesSyncEnabled|Boolean|**TODO: Add Description** Optional.|
|operatingSystem|String|**TODO: Add Description** Optional.|
|operatingSystemVersion|String|**TODO: Add Description** Optional.|
|organizationalUnit|String|**TODO: Add Description** Optional.|
|physicalIds|String collection|**TODO: Add Description** Required.|
|profileType|String|**TODO: Add Description** Optional.|
|registrationDateTime|DateTimeOffset|**TODO: Add Description** Optional.|
|systemLabels|String collection|**TODO: Add Description** Required.|
|trustType|String|**TODO: Add Description** Optional.|
|userCertificate|String|**TODO: Add Description** Optional.|



## Response

If successful, this method returns a `200 OK` response code and an updated [device](../resources/device.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_device"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/devices/{devicesId}
Content-Type: application/json
Content-length: 1900

{
  "@odata.type": "#microsoft.graph.device",
  "deletedDateTime": "String (timestamp)",
  "accountEnabled": "Boolean",
  "alternativeSecurityIds": [
    {
      "@odata.type": "microsoft.graph.alternativeSecurityId"
    }
  ],
  "approximateLastSignInDateTime": "String (timestamp)",
  "capabilities": [
    "String"
  ],
  "compliantApplications": [
    {
      "@odata.type": "microsoft.graph.compliantApplication"
    }
  ],
  "compliantApplicationsManagementAppId": "String",
  "complianceExpirationDateTime": "String (timestamp)",
  "customSecurityAttributes": {
    "@odata.type": "microsoft.graph.customSecurityAttributeValue"
  },
  "deviceCategory": "String",
  "deviceId": "String",
  "deviceKeys": [
    {
      "@odata.type": "microsoft.graph.deviceKey"
    }
  ],
  "deviceMetadata": "String",
  "deviceOwnership": "String",
  "deviceSystemMetadata": {
    "@odata.type": "microsoft.graph.keyValue"
  },
  "deviceVersion": "Integer",
  "displayName": "String",
  "domainName": "String",
  "enrollmentProfileName": "String",
  "enrollmentType": "String",
  "extensionAttributes": {
    "@odata.type": "microsoft.graph.onPremisesExtensionAttributes"
  },
  "exchangeActiveSyncIds": [
    "String"
  ],
  "hostnames": [
    "String"
  ],
  "isCompliant": "Boolean",
  "isManaged": "Boolean",
  "isManagementRestricted": "Boolean",
  "isRooted": "Boolean",
  "localCredentials": "String",
  "managementType": "String",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": "Boolean",
  "operatingSystem": "String",
  "operatingSystemVersion": "String",
  "organizationalUnit": "String",
  "physicalIds": [
    "String"
  ],
  "profileType": "String",
  "registrationDateTime": "String (timestamp)",
  "systemLabels": [
    "String"
  ],
  "trustType": "String",
  "userCertificate": "String"
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
  "@odata.type": "#microsoft.graph.device",
  "id": "f8331ab3-1ab3-f833-b31a-33f8b31a33f8",
  "deletedDateTime": "String (timestamp)",
  "accountEnabled": "Boolean",
  "alternativeSecurityIds": [
    {
      "@odata.type": "microsoft.graph.alternativeSecurityId"
    }
  ],
  "approximateLastSignInDateTime": "String (timestamp)",
  "capabilities": [
    "String"
  ],
  "compliantApplications": [
    {
      "@odata.type": "microsoft.graph.compliantApplication"
    }
  ],
  "compliantApplicationsManagementAppId": "String",
  "complianceExpirationDateTime": "String (timestamp)",
  "customSecurityAttributes": {
    "@odata.type": "microsoft.graph.customSecurityAttributeValue"
  },
  "deviceCategory": "String",
  "deviceId": "String",
  "deviceKeys": [
    {
      "@odata.type": "microsoft.graph.deviceKey"
    }
  ],
  "deviceMetadata": "String",
  "deviceOwnership": "String",
  "deviceSystemMetadata": {
    "@odata.type": "microsoft.graph.keyValue"
  },
  "deviceVersion": "Integer",
  "displayName": "String",
  "domainName": "String",
  "enrollmentProfileName": "String",
  "enrollmentType": "String",
  "extensionAttributes": {
    "@odata.type": "microsoft.graph.onPremisesExtensionAttributes"
  },
  "exchangeActiveSyncIds": [
    "String"
  ],
  "hostnames": [
    "String"
  ],
  "isCompliant": "Boolean",
  "isManaged": "Boolean",
  "isManagementRestricted": "Boolean",
  "isRooted": "Boolean",
  "localCredentials": "String",
  "managementType": "String",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": "Boolean",
  "operatingSystem": "String",
  "operatingSystemVersion": "String",
  "organizationalUnit": "String",
  "physicalIds": [
    "String"
  ],
  "profileType": "String",
  "registrationDateTime": "String (timestamp)",
  "systemLabels": [
    "String"
  ],
  "trustType": "String",
  "userCertificate": "String"
}
```
