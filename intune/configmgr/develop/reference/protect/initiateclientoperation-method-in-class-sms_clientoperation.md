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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
