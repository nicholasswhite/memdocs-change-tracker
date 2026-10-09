---
description: The ImportForUser Windows Management Instrumentation class method, in Configuration Manager, imports a certificate for a user, encrypted by using a password.
title: "ImportForUser Method in Class SMS_ClientPfxCertificate"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
---

# ImportForUser Method in Class SMS_ClientPfxCertificate

The `ImportForUser` Windows Management Instrumentation (WMI) class method, in Configuration Manager, imports a certificate for a user, encrypted by using a password.

## Syntax

```
sint32 ImportForUser(
     String ProfileName,
     String UserName,
     String EncryptedPfxBlob,
     String Password
);

```

#### Parameters

`ProfileName` Data type: `String`

Qualifiers: [in]

The profile name.

`UserName` Data type: `String`

Qualifiers: [in]

The user name.

`EncryptedPfxBlob` Data type: `String`

Qualifiers: [in]

The encrypted blob.

`Password` Data type: `String`

Qualifiers: [in]

The password used to encrypt the certificate.

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
