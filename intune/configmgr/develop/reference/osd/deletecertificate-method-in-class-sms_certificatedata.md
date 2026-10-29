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
