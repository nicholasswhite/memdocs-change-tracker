---
title: "CancelClientOperation Method in Class SMS_ClientOperation"
description: The CancelClientOperation Windows Management Instrumentation (WMI) class method cancels a client operation.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CancelClientOperation Method in Class SMS_ClientOperation

The `CancelClientOperation` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that cancels a client operation.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 CancelClientOperation
{
    [IN]    UInt32 OperationID
};
```

## Parameters

`OperationID` Data type: `UInt32`

Qualifiers: [id("0"), in]

OperationID.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
