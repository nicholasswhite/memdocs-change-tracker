---
description: Learn how to set the fallback time, in minutes, for a distribution point (DP) in Configuration Manager.
title: "FallbackDP Method in Class SMS_BoundaryGroupRelationships"
ms.date: "2017-03-13T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# FallbackDP Method in Class SMS_BoundaryGroupRelationships

The `FallbackDP` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the fallback time, in minutes, for a distribution point (DP). The default value is 120.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 FallbackDP();
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
