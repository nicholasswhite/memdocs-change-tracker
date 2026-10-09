---
title: "DetermineIfRebootPending Method in Class CCM_ClientUtilities"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn how DetermineIfRebootPending is simplified from Managed Object Format code and defines the method.
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

# DetermineIfRebootPending Method in Class CCM_ClientUtilities

The `DetermineIfRebootPending` Windows Management Instrumentation (WMI) class method in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 DetermineIfRebootPending
{
    [OUT]   Boolean RebootPending
    [OUT]   Boolean IsHardRebootPending
    [OUT]   Boolean InGracePeriod
    [OUT]   DateTime DisableHideTime
    [OUT]   DateTime RebootDeadline
};
```

## Parameters

`RebootPending` Data type: `Boolean`

Qualifiers: [id("0"), out]

RebootPending.

`IsHardRebootPending` Data type: `Boolean`

Qualifiers: [id("1"), out]

IsHardRebootPending.

`InGracePeriod` Data type: `Boolean`

Qualifiers: [id("2"), out]

InGracePeriod.

`DisableHideTime` Data type: `DateTime`

Qualifiers: [id("3"), out]

DisableHideTime.

`RebootDeadline` Data type: `DateTime`

Qualifiers: [id("4"), out]

RebootDeadline.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
