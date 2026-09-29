---
title: "SetIsExpired Method in Class SMS_ApplicationLatest"
description: In Configuration Manager, the SetIsExpired WMI class method sets the expired status of this application.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SetIsExpired Method in Class SMS_ApplicationLatest

The `SetIsExpired` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets the expired status of this application.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 SetIsExpired (
     boolean Expired
);
```

#### Parameters

`Expired` Data type: `Boolean`

Qualifiers: [in]

`true` to set the state to expired. The default value is `true`.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ApplicationLatest Server WMI Class](sms_applicationlatest-server-wmi-class.md)
