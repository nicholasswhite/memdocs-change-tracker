---
description: Article outlining how to delete a certificate for a user with DeleteForUser class method in Configuration Manager.
title: "DeleteForUser Method in Class SMS_ClientPfxCertificate"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# DeleteForUser Method in Class SMS_ClientPfxCertificate

The `DeleteForUse` Windows Management Instrumentation (WMI) class method, in Configuration Manager, deletes a certificate for a user.

## Syntax

```
 sint32 DeleteForUser(
     String ProfileName,
     String UserName,
     String Thumbprint
);

```

#### Parameters

`ProfileName` Data type: `String`

Qualifiers: [in]

The profile name.

`UserName` Data type: `String`

Qualifiers: [in]

The user name.

`Thumbprint` Data type: `String`

Qualifiers: [in]

The thumbprint for the certificate.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ClientPfxCertificate Server WMI Class](sms_clientpfxcertificate-server-wmi-class.md)
