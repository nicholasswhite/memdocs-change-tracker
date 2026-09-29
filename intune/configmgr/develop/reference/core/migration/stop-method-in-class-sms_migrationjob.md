---
description: Learn how to stop the migration job in Configuration Manager using the Stop class method.
title: "Stop Method in Class SMS_MigrationJob"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Stop Method in Class SMS_MigrationJob

The `Stop` Windows Management Instrumentation (WMI) class method, in Configuration Manager, stops the migration job.

> [!IMPORTANT]
>
> This requires the Manage Migration Job right.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 Stop();
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MigrationJob Server WMI Class](sms_migrationjob-server-wmi-class.md)
