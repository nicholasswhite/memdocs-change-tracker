---
title: "ReloadImageProperties Method in Class SMS_ImagePackage"
description: In Configuration Manager, the ReloadImageProperties WMI class method reloads image metadata from an image source .wim file.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ReloadImageProperties Method in Class SMS_ImagePackage

The `ReloadImageProperties` Windows Management Instrumentation (WMI) class method, in Configuration Manager, reloads image metadata from an image source .wim file and synchronizes the metadata with the database.

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

For an example of the use of this method, see [How to Update an Operating System Image Package in Configuration Manager](../../osd/how-to-update-an-operating-system-image-package.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ImagePackage Server WMI Class](sms_imagepackage-server-wmi-class.md) [GetImageProperties Method in Class SMS_ImagePackage](getimageproperties-method-in-class-sms_imagepackage.md) [How to Update an Operating System Image Package in Configuration Manager](../../osd/how-to-update-an-operating-system-image-package.md)
