---
title: Close Method in Class SMS_CHAlert
description: In Configuration Manager, the Close Windows Management Instrumentation class method postpones the alert.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Close Method in Class SMS_CHAlert

The `Close` Windows Management Instrumentation (WMI) class method, in Configuration Manager, postpones the alert.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 Close(
     string Comments,
     string SkipUntil
);
```

#### Parameters

`Comments` Data type: `String`

Qualifiers: `[in, optional]`

Administrator-supplied comments for the postpone action.

`SkipUntil` Data type: `DateTime`

Qualifiers: `[out, optional]`

Don't start the evaluation until the specified time.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_Alert server WMI class](sms_alert-server-wmi-class.md)
