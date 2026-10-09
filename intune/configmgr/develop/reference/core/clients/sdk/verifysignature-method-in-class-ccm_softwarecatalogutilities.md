---
title: "VerifySignature Method in Class CCM_SoftwareCatalogUtilities"
description: In Configuration Manager, the VerifySignature WMI class method verifies the data signature.
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

# VerifySignature Method in Class CCM_SoftwareCatalogUtilities

The `VerifySignature` Windows Management Instrumentation (WMI) class method in Configuration Manager that verifies the data signature.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 VerifySignature
{
    [IN]    String Data
    [IN]    String DataSignature
    [IN]    String WebServiceID
    [IN]    Boolean VerifyUserAndTimestamp
    [OUT]   Boolean SignatureVerificationPassed
};
```

## Parameters

`Data` Data type: `String`

Qualifiers: [id("0"), in]

Data to verify.

`DataSignature` Data type: `String`

Qualifiers: [id("1"), in]

Data signature.

`WebServiceID` Data type: `String`

Qualifiers: [id("2"), in]

Web Service identifier.

`VerifyUserAndTimestamp` Data type: `Boolean`

Qualifiers: [id("3"), in]

`true` to verify the user and timestamp.

`SignatureVerificationPassed` Data type: `Boolean`

Qualifiers: [id("4"), out]

`true` if the data signature is valid.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
