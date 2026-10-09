---
title: "CancelWipe Method in Class SMS_DeviceMethods"
description: The CancelWipe Windows Management Instrumentation (WMI) class method cancels a pending wipe request on mobile devices or Exchange ActiveSync devices.
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

# CancelWipe Method in Class SMS_DeviceMethods

The `CancelWipe` Windows Management Instrumentation (WMI) class method, in Configuration Manager, cancels a pending wipe request on mobile devices or Exchange ActiveSync devices.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 CancelWipe(
   UInt32 ResourceId
);
```

#### Parameters

`ResourceId` Data type: `UInt32`

Qualifiers: [in]

Identifier of the resource for which to cancel the wipe.

## Return Values

An `SInt32`data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## See Also

[SMS_DeviceMethods Server WMI Class](sms_devicemethods-server-wmi-class.md)
