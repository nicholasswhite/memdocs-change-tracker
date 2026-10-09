---
title: "UploadToken Method in Class SMS_MDMAppleVppToken"
description: The UploadToken WMI class method uploads an Apple Volume Purchase Program (VPP) token to Microsoft Intune.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# UploadToken Method in Class SMS_MDMAppleVppToken

The `UploadToken` Windows Management Instrumentation (WMI) class method, in Configuration Manager, uploads an Apple Volume Purchase Program (VPP) token to Microsoft Intune.

## Syntax

```
sint32 UploadToken(
     String TokenID,
     String VppToken,
     String OrganizationName,
     String ExpirationDate
);

```

#### Parameters

`TokenID` Data type: `String`

Qualifiers: [in]

The ID of the Apple VPP token.

`VppToken` Data type: `String`

Qualifiers: [in]

Name of the token.

`OrganizationName` Data type: `String`

Qualifiers: [in]

Organization name for the token.

`ExpirationDate` Data type: `String`

Qualifiers: [in]

Expiration date of the token.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MDMAppleVppToken Server WMI Class](sms_mdmapplevpptoken-server-wmi-class.md)
