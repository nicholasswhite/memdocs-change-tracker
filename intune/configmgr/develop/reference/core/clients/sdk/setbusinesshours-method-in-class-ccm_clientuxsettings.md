---
title: "SetBusinessHours Method in Class CCM_ClientUXSettings"
description: Learn how the SetBusinessHours Windows Management Instrumentation (WMI) class method in Configuration Manager that sets the values for business hours.
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

# SetBusinessHours Method in Class CCM_ClientUXSettings

The `SetBusinessHours` Windows Management Instrumentation (WMI) class method in Configuration Manager that sets the values for business hours.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 SetBusinessHours
{
    [IN]    UInt32 WorkingDays
    [IN]    UInt32 StartTime
    [IN]    UInt32 EndTime
};
```

## Parameters

`WorkingDays` Data type: `UInt32`

Qualifiers: [id("0"), in]

Working days.

`StartTime` Data type: `UInt32`

Qualifiers: [id("1"), in]

Start time.

`EndTime` Data type: `UInt32`

Qualifiers: [id("2"), in]

End time.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
