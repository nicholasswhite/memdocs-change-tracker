---
title: "QueueRequestedAppPolicy Method in Class CCM_RequestedAppPolicy"
description: In Configuration Manager, the QueueRequestedAppPolicy Windows Management Instrumentation class method that queues an application policy request.
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

# QueueRequestedAppPolicy Method in Class CCM_RequestedAppPolicy

The `QueueRequestedAppPolicy` Windows Management Instrumentation (WMI) class method in Configuration Manager that queues and application policy request.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 QueueRequestedAppPolicy
{
    [IN]    String PolicyId
    [IN]    String PolicyRevision
    [IN]    String Id
    [IN]    UInt32 EnforcePreference
};
```

## Parameters

`PolicyId` Data type: `String`

Qualifiers: [id("0"), in]

Policy identifier.

`PolicyRevision` Data type: `String`

Qualifiers: [id("1"), in]

Policy revision.

`Id` Data type: `String`

Qualifiers: [id("2"), in]

Identifier.

`EnforcePreference` Data type: `UInt32`

Qualifiers: [id("3"), in]

Enforce preference. Possible values are:

| Value | Enforce preference |
| --- | --- |
| 0 | Immediate |
| 1 | Non-Business Hours |
| 2 | Admin Schedule |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
