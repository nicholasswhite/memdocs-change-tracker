---
title: "ChangeOwnership Method in Class SMS_Collection"
description: Learn how the ChangeOwnership Windows Management Instrumentation (WMI) class method, in Configuration Manager, changes ownership of the devices.
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

# ChangeOwnership Method in Class SMS_Collection

The `ChangeOwnership` Windows Management Instrumentation (WMI) class method, in Configuration Manager, changes ownership of the devices.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ChangeOwnership(
     UInt32 ResourceIDs[],
     UInt32 DeviceOwner
     SInt32 ReturnValue
);
```

#### Parameters

`ResourceIDs` Data type: `UInt32` Array

Qualifiers: [in]

IDs of member resources.

`DeviceOwner` Data type: `UInt32`

Qualifiers: [in]

The new owner of the machines.

| Value | Device owner |
| --- | --- |
| 1 | Company |
| 2 | Personal |

`ReturnValue` Data type: `SInt32`

Qualifiers: [out]

The number of devices that were successfully reassigned ownership.

> [!IMPORTANT]
>
> Even if there is an error, some devices may still get reassigned ownership.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) [SMS_Site Server WMI Class](../../servers/configure/sms_site-server-wmi-class.md)
