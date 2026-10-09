---
title: "InitiateClientOperation Method in Class SMS_ClientOperation"
description: In Configuration Manager, the InitiateClientOperation WMI class method initiates a client operation.
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

# InitiateClientOperation Method in Class SMS_ClientOperation

The `InitiateClientOperation` Windows Management Instrumentation (WMI) class method in Configuration Manager that initiates a client operation.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 InitiateClientOperation
{
    [IN]    UInt32 Type
    [IN]    String TargetCollectionID
    [IN]    UInt32 RandomizationWindow
    [IN]    UInt32 TargetResourceIDs[]
    [OUT]   UInt32 OperationID
};
```

## Parameters

`Type` Data type: `UInt32`

Qualifiers: [id("0"), in]

Type.

`TargetCollectionID` Data type: `String`

Qualifiers: [id("1"), in]

TargetCollectionID.

`RandomizationWindow` Data type: `UInt32`

Qualifiers: [id("2"), in, optional]

RandomizationWindow.

`TargetResourceIDs` Data type: `UInt32 Array`

Qualifiers: [id("3"), in, optional]

TargetResourceIDs.

`OperationID` Data type: `UInt32`

Qualifiers: [id("4"), out]

OperationID.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
