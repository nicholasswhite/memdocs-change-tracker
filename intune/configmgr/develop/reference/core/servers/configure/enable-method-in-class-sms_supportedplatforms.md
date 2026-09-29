---
description: The Enable Windows Management Instrumentation (WMI) class method, in Configuration Manager, enables or disables the platforms.
title: "Enable Method in Class SMS_SupportedPlatforms"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Enable Method in Class SMS_SupportedPlatforms

The `Enable` Windows Management Instrumentation (WMI) class method, in Configuration Manager, enables or disables the platforms.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 Enable(
     boolean IsSupported
);
```

#### Parameters

`IsSupported` Data type: `Boolean`

Qualifiers: `[in]`

`true` if the platforms are enabled. The default value is `true`.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Application Server WMI Class](../../../apps/sms_application-server-wmi-class.md)
