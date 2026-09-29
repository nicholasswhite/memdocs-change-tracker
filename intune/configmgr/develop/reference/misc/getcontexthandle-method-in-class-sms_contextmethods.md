---
title: "GetContextHandle Method in Class SMS_ContextMethods"
description: The GetContextHandle method, in Configuration Manager, stores context objects on the server.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetContextHandle Method in Class SMS_ContextMethods

The `GetContextHandle` method, in Configuration Manager, stores context objects on the server.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetContextHandle(
      String ContextHandle
);
```

#### Parameters

`ContextHandle` Data type: `String`

Qualifiers: [out]

Context handle that identifies the cached context object on the server.

## Return Values

An `SInt32` data type that indicates 0 for success or non-zero for failure.

## Remarks

Use this method to replace the contents of your context object with the object indicated by the retrieved context handle. Storing context object data on the server saves network bandwidth for client applications that repeatedly call the SMS Provider using a large number of context qualifiers or a large amount of qualifier data.

For a complete description of the steps required to use this optimization technique, see the ContextHandle qualifier in [Configuration Manager Context Qualifiers](../../core/understand/context-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ContextMethods Class](sms_contextmethods-server-wmi-class.md) [ClearContextHandle](clearcontexthandle-method-in-class-sms_contextmethods.md)
