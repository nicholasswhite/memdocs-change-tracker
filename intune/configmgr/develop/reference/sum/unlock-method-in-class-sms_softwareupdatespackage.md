---
description: The Unlock Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the source site to the current site, unlocking the software updates package.
title: "Unlock Method in Class SMS_SoftwareUpdatesPackage"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3


ms.service: configuration-manager
---

# Unlock Method in Class SMS_SoftwareUpdatesPackage

The `Unlock` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the source site to the current site, unlocking the software updates package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 Unlock();  
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdatesPackage Server WMI Class](sms_softwareupdatespackage-server-wmi-class.md)  
 [RefreshPkgSource Method in Class SMS_SoftwareUpdatesPackage](refreshpkgsource-method-in-class-sms_softwareupdatespackage.md)  
 [SetSourceSite Method in Class SMS_SoftwareUpdatesPackage](setsourcesite-method-in-class-sms_softwareupdatespackage.md)  
 [ValidateNewPackageSource Method in Class SMS_SoftwareUpdatesPackage](validatenewpackagesource-method-in-class-sms_softwareupdatespackage.md)
