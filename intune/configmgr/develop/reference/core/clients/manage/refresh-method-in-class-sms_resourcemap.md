---
title: "Refresh Method in Class SMS_ResourceMap"
description: The Refresh Windows Management Instrumentation class method, in Configuration Manager, updates resource and inventory class definitions.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Refresh Method in Class SMS_ResourceMap

The `Refresh` Windows Management Instrumentation (WMI) class method, in Configuration Manager, updates resource (classes derived from [SMS_R_System Server WMI Class](sms_r_system-server-wmi-class.md)) and inventory (classes derived from [SMS_G_System_Current Server WMI Class](sms_g_system_current-server-wmi-class.md)) class definitions.

The following syntax is simplified from Manage Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 Refresh();
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ResourceMap Server WMI Class](sms_resourcemap-server-wmi-class.md)
