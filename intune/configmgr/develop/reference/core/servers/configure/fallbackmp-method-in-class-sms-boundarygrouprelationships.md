---
title: "FallbackMP Method in Class SMS_BoundaryGroupRelationships"
description: In Configuration Manager, the FallbackMP Windows Management Instrumentation class method sets the fallback time in minutes for a management point with the default value of 120.
ms.date: "2017-03-13T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# FallbackMP Method in Class SMS_BoundaryGroupRelationships

The `FallbackMP` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the fallback time, in minutes, for a management point (MP). The default value is 120.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 FallbackMP();
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
