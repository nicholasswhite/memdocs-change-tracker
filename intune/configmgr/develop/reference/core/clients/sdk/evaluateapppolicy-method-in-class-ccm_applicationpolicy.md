---
title: "EvaluateAppPolicy Method in Class CCM_ApplicationPolicy"
description: Learn how the EvaluateAppPolicy Windows Management Instrumentation (WMI) class method, in Configuration Manager, that evaluates application policy.
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

# EvaluateAppPolicy Method in Class CCM_ApplicationPolicy

The `EvaluateAppPolicy` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that evaluates application policy.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 EvaluateAppPolicy
{
    [IN]    String PolicyId
    [IN]    String PolicyRevision
    [IN]    Boolean IsMachineTarget
    [IN]    String Priority
    [IN]    Boolean IsEnforceAction
    [IN]    String MTCToken
    [IN]    String SDKCallerId
    [OUT]   String JobId
};
```

## Parameters

`PolicyId` Data type: `String`

Qualifiers: [id("0"), in]

Policy identifier.

`PolicyRevision` Data type: `String`

Qualifiers: [id("1"), in]

Policy revision.

`IsMachineTarget` Data type: `Boolean`

Qualifiers: [id("2"), in]

`True` if this is a device targeted application.

`Priority` Data type: `String`

Qualifiers: [id("3"), in, valuemap]

Priority. Possible values are:

| Value |
| --- |
| Foreground |
| High |
| Normal |
| Low |

`IsEnforceAction` Data type: `Boolean`

Qualifiers: [id("4"), in]

`True` if the action will be enforced.

`MTCToken` Data type: `String`

Qualifiers: [id("5"), in]

MTC token.

`SDKCallerId` Data type: `String`

Qualifiers: [id("6"), in]

SDK caller identifier.

`JobId` Data type: `String`

Qualifiers: [id("7"), out]

Job identifier.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
