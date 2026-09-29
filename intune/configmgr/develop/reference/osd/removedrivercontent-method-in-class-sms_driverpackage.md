---
title: "RemoveDriverContent Method in Class SMS_DriverPackage"
description: In Configuration Manager, the RemoveDriverContent WMI class method removes the specified driver from the driver package.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# RemoveDriverContent Method in Class SMS_DriverPackage

The `RemoveDriverContent` Windows Management Instrumentation (WMI) class method, in Configuration Manager, removes the specified driver from the driver package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RemoveDriverContent(
     UInt32 ContentIDs[],
     Boolean bRefreshDPs
);
```

#### Parameters

`ContentIDs` Data type: `UInt32` Array

Qualifiers: [in]

The IDs for driver content to remove from the driver package.

`bRefreshDPs` Data type: `Boolean`

Qualifiers: [in, optional]

`true`, by default, to replicate package changes to the distribution points.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_DriverPackage Server WMI Class](sms_driverpackage-server-wmi-class.md) [AddDriverContent Method in Class SMS_DriverPackage](adddrivercontent-method-in-class-sms_driverpackage.md) [RebuildPackage Method in Class SMS_DriverPackage](rebuildpackage-method-in-class-sms_driverpackage.md) [ValidateNewPackageSource Method in Class SMS_DriverPackage](validatenewpackagesource-method-in-class-sms_driverpackage.md)
