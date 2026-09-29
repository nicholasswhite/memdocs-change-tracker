---
title: "UpdateConsoleUsageData Method in Class SMS_Site"
description: In Configuration Manager, the UpdateConsoleUsageData WMI class method updates console usage data received from console connections.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# UpdateConsoleUsageData Method in Class SMS_Site

The `UpdateConsoleUsageData` Windows Management Instrumentation (WMI) class method, in Configuration Manager, updates console usage data received from console connections.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 UpdateConsoleUsageData (
    SMS_ConsoleUsageData ConsoleUsageData
);

```

#### Parameters

`ConsoleUsageData` Data type: `SMS_ConsoleUsageData`

Qualifiers: [in]

Console usage data.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Site Server WMI Class](sms_site-server-wmi-class.md)
