---
title: "RebuildPackage Method in Class SMS_SoftwareUpdatesPackage"
description: The RebuildPackage WMI class method brings the software updates package to its expected state if files are found to be corrupt or have been deleted.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# RebuildPackage Method in Class SMS_SoftwareUpdatesPackage

The `RebuildPackage` Windows Management Instrumentation (WMI) class method, in Configuration Manager, brings the software updates package to its expected state if files are found to be corrupt or have been deleted.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RebuildPackage(
     String ContentSourcePath
);
```

#### Parameters

`ContentSourcePath` Data type: `String`

Qualifiers: [in, optional]

Source path where the content files are located.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdatesPackage Server WMI Class](sms_softwareupdatespackage-server-wmi-class.md) [AddUpdateContent Method in Class SMS_SoftwareUpdatesPackage](addupdatecontent-method-in-class-sms_softwareupdatespackage.md) [RemoveContent Method in Class SMS_SoftwareUpdatesPackage](removecontent-method-in-class-sms_softwareupdatespackage.md)
