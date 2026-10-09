---
title: "Unlock Method in Class SMS_DeviceSettingPackage"
description: Sets the source site to the current site, unlocking the device setting package in Configuration Manager.
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

# Unlock Method in Class SMS_DeviceSettingPackage

The `Unlock` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the source site to the current site, unlocking the device setting package.

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

## See Also

[SMS_DeviceSettingPackage Server WMI Class](sms_devicesettingpackage-server-wmi-class.md) [RefreshPkgSource Method in Class SMS_DeviceSettingPackage](refreshpkgsource-method-in-class-sms_devicesettingpackage.md) [SetSourceSite Method in Class SMS_DeviceSettingPackage](setsourcesite-method-in-class-sms_devicesettingpackage.md)
