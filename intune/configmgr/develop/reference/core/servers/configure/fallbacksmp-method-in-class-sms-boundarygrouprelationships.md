---
description: Learn how to set the fallback time, in minutes, for a state migration point (SMP) using FallbackSMP.
title: "FallbackSMP Method in Class SMS_BoundaryGroupRelationships"
ms.date: "2017-03-13T00:00:00Z"
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

# FallbackSMP Method in Class SMS_BoundaryGroupRelationships

The `FallbackSMP` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the fallback time, in minutes, for a state migration point (SMP). The default value is 120.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 FallbackSMP();
```

### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BoundaryGroupRelationships Server WMI Class](sms-boundarygrouprelationships-server-wmi-class.md)
