---
title: GetSummary Method in Class SMS_AIHardwareRequirements
description: In Configuration Manager, the GetSummary WMI class method provides a summary count of validated and user-defined state items in the SMS_AIHardwareRequirements class.
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

# GetSummary Method in Class SMS_AIHardwareRequirements

The `GetSummary` Windows Management Instrumentation (WMI) class method, in Configuration Manager, provides a summary count of validated and user-defined state items in the `SMS_AIHardwareRequirements` class.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetSummary(
     UInt32 Validated,
     UInt32 UserDefined
);
```

#### Parameters

`Validated` Data type: `UInt32`

Qualifiers: [out]

Count of Microsoft-defined items.

`UserDefined` Data type: `UInt32`

Qualifiers: [out]

Count of user-defined items.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_AIHardwareRequirements Server WMI Class](sms_aihardwarerequirements-server-wmi-class.md)
