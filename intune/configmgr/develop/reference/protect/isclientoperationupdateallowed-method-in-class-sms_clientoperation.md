---
title: "IsClientOperationUpdateAllowed Method in Class SMS_ClientOperation"
description: The IsClientOperationUpdateAllowed Windows Management Instrumentation (WMI) class method, in Configuration Manager, that checks whether a user has permission to update an operation. The following syntax is simplified from Managed Object Format (MOF) code and defines the method.
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

# IsClientOperationUpdateAllowed Method in Class SMS_ClientOperation

The `IsClientOperationUpdateAllowed` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that checks whether a user has permission to update an operation.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 IsClientOperationUpdateAllowed
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
