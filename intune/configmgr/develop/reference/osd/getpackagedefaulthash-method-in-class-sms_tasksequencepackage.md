---
title: "GetPackageDefaultHash Method in Class SMS_TaskSequencePackage"
description: The `GetPackageDefaultHash` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the hash of a Configuration Manager package.
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

# GetPackageDefaultHash Method in Class SMS_TaskSequencePackage

The `GetPackageDefaultHash` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the hash of a Configuration Manager package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetPackageDefaultHash(
      String PackageID,
      UInt32 SourceVersion,
      String Hash,
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
