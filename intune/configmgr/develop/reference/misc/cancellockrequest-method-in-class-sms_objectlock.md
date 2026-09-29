---
title: "CancelLockRequest Method in Class SMS_ObjectLock"
description: The CancelLockRequest Windows Management Instrumentation (WMI) class method cancels a lock request.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CancelLockRequest Method in Class SMS_ObjectLock

The `CancelLockRequest` Windows Management Instrumentation (WMI) class method, in Configuration Manager, cancels a lock request.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 CancelLockRequest(
    string RequestID
);
```

#### Parameters

`RequestID` Data type: `String`

Qualifiers: [in]

Unique identifier of the request.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ObjectLock Server WMI Class](sms_objectlock-server-wmi-class.md)
