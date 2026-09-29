---
title: "Approve Method in Class SMS_UserApplicationRequest"
description: The `Approve` Windows Management Instrumentation (WMI) class method, in Configuration Manager, approves user application requests.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Approve Method in Class SMS_UserApplicationRequest

The `Approve` Windows Management Instrumentation (WMI) class method, in Configuration Manager, approves user application requests.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 Approve(
     string Comments
);
```

#### Parameters

`Comments` Data type: `String` Array

Qualifiers: [in, SizeLimit("2000")]

Comments regarding the approval of the application request.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_UserApplicationRequest Server WMI Class](sms_userapplicationrequest-server-wmi-class.md)
