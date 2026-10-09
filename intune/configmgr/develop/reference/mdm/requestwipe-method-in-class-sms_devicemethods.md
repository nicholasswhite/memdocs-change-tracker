---
description: Learn how to use Configuration Manager RequestWipe Windows Management Instrumentation (WMI) class method to remove Microsoft Exchange and Configuration Manager software from the mobile device or Exchange ActiveSync device.
title: "RequestWipe Method in Class SMS_DeviceMethods"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/390894b2-8646-4f7e-b8cd-2209156272a9
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12b23b77-ab37-4318-a036-4f6690586386
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# RequestWipe Method in Class SMS_DeviceMethods

The `RequestWipe` Windows Management Instrumentation (WMI) class method, in Configuration Manager, removes Microsoft Exchange and Configuration Manager software from the mobile device or Exchange ActiveSync device.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RequestWipe(
   UInt32 ResourceId
   String EASIdentities[]
);
```

#### Parameters

`ResourceId` Data type: `UInt32`

Qualifiers: [in]

ID of the resource to remove software from.

`EASIdentities` Data type: `String` Array

Qualifiers: [in]

Array of Exchange ActiveSync identities.

## Return Values

An `SInt32`data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## See Also

[SMS_DeviceMethods Server WMI Class](sms_devicemethods-server-wmi-class.md)
