---
title: "CancelRetire Method in Class SMS_DeviceMethods"
description: The CancelRetire WMI class method cancels the retirement of this device from Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CancelRetire Method in Class SMS_DeviceMethods

The `CancelRetire` Windows Management Instrumentation (WMI) class method, in Configuration Manager, cancels the retirement of this device from Configuration Manager (the device will remain managed by Configuration Manager).

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 CancelRetire(
   UInt32 ResourceId
);
```

#### Parameters

`ResourceId` Data type: `UInt32`

Qualifiers: [in]

ID of the resource.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## See Also

[SMS_DeviceMethods Server WMI Class](sms_devicemethods-server-wmi-class.md)
