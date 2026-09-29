---
title: "RebuildPackage Method in Class SMS_DriverPackage"
description: The RebuildPackage Windows Management Instrumentation (WMI) class method, in Configuration Manager, restores the contents for the driver package.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# RebuildPackage Method in Class SMS_DriverPackage

The `RebuildPackage` Windows Management Instrumentation (WMI) class method, in Configuration Manager, restores the contents for the driver package.

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

[SMS_DriverPackage Server WMI Class](sms_driverpackage-server-wmi-class.md) [AddDriverContent Method in Class SMS_DriverPackage](adddrivercontent-method-in-class-sms_driverpackage.md) [RemoveDriverContent Method in Class SMS_DriverPackage](removedrivercontent-method-in-class-sms_driverpackage.md) [ValidateNewPackageSource Method in Class SMS_DriverPackage](validatenewpackagesource-method-in-class-sms_driverpackage.md)
