---
title: "DeleteCertificate Method in Class SMS_CertificateData"
description: In Configuration Manager, the DeleteCertificate WMI class method that deletes the certificate from the database.
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

# DeleteCertificate Method in Class SMS_CertificateData

The `DeleteCertificate` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that deletes the certificate from the database.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 DeleteCertificate(
    [IN] UInt32 CertType
);

```

## Parameters

`CertType` Data type: `UInt32`

Qualifiers: [in]

Certificate type.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
