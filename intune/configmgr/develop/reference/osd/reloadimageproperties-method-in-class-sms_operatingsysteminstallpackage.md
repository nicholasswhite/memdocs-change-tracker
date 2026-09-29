---
description: Learn how to use the ReloadImageProperties method in class SMS_OperatingSystemInstallPackage reload metadata from the source .wim file and synchronize the metadata with the database.
title: "ReloadImageProperties Method in Class SMS_OperatingSystemInstallPackage"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ReloadImageProperties Method in Class SMS_OperatingSystemInstallPackage

The `ReloadImageProperties` Windows Management Instrumentation WMI class method, in Configuration Manager, reloads metadata from the source .wim file and synchronizes the metadata with the database.

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

Your application uses this method to update the .wim file associated with the operating system install package. The update is based on the location defined in the `PkgSourcePath` property of [SMS_OperatingSystemInstallPackage Server WMI Class](sms_operatingsysteminstallpackage-server-wmi-class.md).

The application must:

1. Establish a connection to the SMS Provider. For more information, see About the SMS Provider in Configuration Manager.
2. Get the `SMS_OperatingSystemInstallPackage` object to update.
3. Call the `ReloadImageProperties` method.
4. Commit the `SMS_OperatingSystemInstallPackage` object.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_OperatingSystemInstallPackage Server WMI Class](sms_operatingsysteminstallpackage-server-wmi-class.md) [GetImageProperties Method in Class SMS_OperatingSystemInstallPackage](getimageproperties-method-in-class-sms_operatingsysteminstallpackage.md)
