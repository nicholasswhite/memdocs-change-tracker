---
description: Learn how to get the hash of a Configuration Manager package using GetPackageHash class method in Configuration Manager.
title: "GetPackageHash Method in Class SMS_TaskSequencePackage"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# GetPackageHash Method in Class SMS_TaskSequencePackage

The `GetPackageHash` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the hash of a Configuration Manager package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetPackageHash(
      String PackageID,
      UInt32 SourceVersion,
      String Hash,
      UInt32 HashVersion
);
```

#### Parameters

`PackageID` Data type: `String`

Qualifiers: [in]

ID of the task sequence package.

`SourceVersion` Data type: `UInt32`

Qualifiers: [in]

The version of the package available at the site. This version is indicated by the `SourceVersion` property of [SMS_TaskSequencePackage Server WMI Class](sms_tasksequencepackage-server-wmi-class.md).

`Hash` Data type: `String`

Qualifiers: [out]

The hash for the package content.

`HashVersion` Data type: `UInt32`

Qualifiers: [out]

The type of the requested hash which can be one of the following values.

1 - MD5 hash

2 - SHA-1 hash

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_TaskSequencePackage Server WMI Class](sms_tasksequencepackage-server-wmi-class.md)
