---
title: "RemoveBoundary Method in Class SMS_BoundaryGroup"
description: In Configuration Manager, the RemoveBoundary WMI class method removes boundaries from a boundary group.
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

# RemoveBoundary Method in Class SMS_BoundaryGroup

The `RemoveBoundary` Windows Management Instrumentation (WMI) class method, in Configuration Manager, removes boundaries from this boundary group.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RemoveBoundary(
   UInt32 BoundaryID[]
);
```

#### Parameters

`BoundaryID` Data type: `UInt32` Array

Qualifiers: [in]

Unique identifier of the boundary.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BoundaryGroup Server WMI Class](sms_boundarygroup-server-wmi-class.md)
