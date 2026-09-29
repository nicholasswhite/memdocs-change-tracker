---
title: "ReloadImageProperties Method in Class SMS_BootImagePackage"
description: Reloads image metadata from a boot image source .wim file and synchronizes the metadata with the database.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ReloadImageProperties Method in Class SMS_BootImagePackage

The `ReloadImageProperties` Windows Management Instrumentation WMI class method, in Configuration Manager, reloads image metadata from a boot image source .wim file and synchronizes the metadata with the database.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ReloadImageProperties();
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

The application uses this method if the administrator changes the boot image source .wim file outside of the Configuration Manager console. The application should:

1. Establish a connection to the SMS Provider. For more information, see [SMS Provider fundamentals](../../core/understand/sms-provider-fundamentals.md).
2. Obtain the [SMS_BootImagePackage Server WMI Class](sms_bootimagepackage-server-wmi-class.md) object to update.
3. Call `ReloadImageProperties`.
4. Commit the `SMS_BootImagePackage` object.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BootImagePackage Server WMI Class](sms_bootimagepackage-server-wmi-class.md) [UpdateImage Method in Class SMS_BootImagePackage](updateimage-method-in-class-sms_bootimagepackage.md)
