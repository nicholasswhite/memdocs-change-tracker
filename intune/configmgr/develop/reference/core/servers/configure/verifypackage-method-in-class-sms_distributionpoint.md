---
title: "VerifyPackage Method in Class SMS_DistributionPoint"
description: A class method that verifies the integrity of the files in a package by calculating the hash of each file.
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

# VerifyPackage Method in Class SMS_DistributionPoint

The `VerifyPackage` Windows Management Instrumentation (WMI) class method, in Configuration Manager, verifies the integrity of all the files in the package by calculating the hash of each file.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 VerifyPackage(
     string PackageId,
     string NALPath
);
```

#### Parameters

`PackageId` Data type: `String`

Qualifiers: `[in]`

ID for an existing package.

`NALPath` Data type: `String`

Qualifiers: `[in]`

Network abstraction layer (NAL) path to the distribution point server.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Application Server WMI Class](../../../apps/sms_application-server-wmi-class.md)
