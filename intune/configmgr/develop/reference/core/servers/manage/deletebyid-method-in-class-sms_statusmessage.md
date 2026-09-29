---
title: "DeleteByID Method in Class SMS_StatusMessage"
description: Learn how the DeleteByID Windows Management Instrumentation (WMI) class method deletes a group of up to 256 status messages.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# DeleteByID Method in Class SMS_StatusMessage

The `DeleteByID` Windows Management Instrumentation (WMI) class method, in Configuration Manager, deletes a group of up to 256 status messages.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 DeleteByID(
   SInt64 RecordIDs[]
);
```

#### Parameters

`RecordIDs` Data type: `SInt64` Array

Qualifiers: [in, Max(256)]

IDs for the records of the status messages to delete.

## Return Values

A `UInt32` data type that indicates the number of rows deleted.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StatusMessage Server WMI Class](sms_statusmessage-server-wmi-class.md)
