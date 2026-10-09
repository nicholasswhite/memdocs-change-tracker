---
title: "RequestLocksAsync Method in Class SMS_ObjectLock"
description: Learn how to asynchronously acquire locks to edit multiple global objects using RequestLocksAsync class method in Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# RequestLocksAsync Method in Class SMS_ObjectLock

The `RequestLocksAsync` Windows Management Instrumentation (WMI) class method, in Configuration Manager, asynchronously acquires locks to edit multiple global objects.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RequestLocksAsync(
    string ObjectRelPath[],
    boolean RequestTransfer,
    SMS_ObjectLockRequest ObjectLockRequests[]
);
```

#### Parameters

`ObjectRelPath` Data type: `String` Array

Qualifiers: [in]

The paths of the objects for which the locks are requested. `RequestTransfer` Data type: `Boolean`

Qualifiers: [in, optional]

If the lock is not owned by the local site, the lock request should be forwarded to the parent/child site.

`ObjectLockRequests` Data type: `SMS_ObjectLockRequest` Array

Qualifiers: [out]

A WMI class that represents object lock request information.

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
