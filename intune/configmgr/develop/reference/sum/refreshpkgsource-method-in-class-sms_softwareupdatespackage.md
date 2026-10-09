---
title: "RefreshPkgSource Method in Class SMS_SoftwareUpdatesPackage"
description: Refresh the package source at all distribution points. The source version of the package is incremented, and the package content is replicated to child sites.
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

# RefreshPkgSource Method in Class SMS_SoftwareUpdatesPackage

The `RefreshPkgSource` Windows Management Instrumentation (WMI) class method, in Configuration Manager, refreshes the package source at all distribution points. The latest version of the package is copied to all the distribution points of the package. The source version of the package is incremented, and the package content is replicated to child sites.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RefreshPkgSource();
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

Using this method is the only way to force an update of the source files, other than by creating a `RefreshSchedule` value for the package. For information about the `RefreshSchedule` property, see [SMS_PackageBaseclass Server WMI Class](../core/servers/configure/sms_packagebaseclass-server-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdatesPackage Server WMI Class](sms_softwareupdatespackage-server-wmi-class.md) [SetSourceSite Method in Class SMS_SoftwareUpdatesPackage](setsourcesite-method-in-class-sms_softwareupdatespackage.md) [ValidateNewPackageSource Method in Class SMS_SoftwareUpdatesPackage](validatenewpackagesource-method-in-class-sms_softwareupdatespackage.md) [SMS_PackageBaseclass Server WMI Class](../core/servers/configure/sms_packagebaseclass-server-wmi-class.md)
