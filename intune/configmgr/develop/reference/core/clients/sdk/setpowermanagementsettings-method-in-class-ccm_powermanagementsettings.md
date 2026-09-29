---
title: "SetPowerManagementSettings Method in Class CCM_PowerManagementSettings"
description: A class method that sets power management settings on a client.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SetPowerManagementSettings Method in Class CCM_PowerManagementSettings

The `SetPowerManagementSettings` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that sets power management settings on a client.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 SetPowerManagementSettings
{
    [IN]  Boolean IsOptOutFromPowerPlan;
    [OUT] UInt32 ReturnValue;
};
```

## Parameters

`IsOptOutFromPowerPlan` Data type: `Boolean`

Qualifiers: [id("0"), in]

`true` to allow users to exclude their device from power management.

`ReturnValue` Data type: `UInt32`

Qualifiers: [out]

Return value.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
