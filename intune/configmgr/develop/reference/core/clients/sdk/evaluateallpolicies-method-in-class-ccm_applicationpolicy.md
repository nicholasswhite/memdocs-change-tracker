---
title: "EvaluateAllPolicies Method in Class CCM_ApplicationPolicy"
description: A Windows Management Instrumentation class method that evaluates all policies.
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

# EvaluateAllPolicies Method in Class CCM_ApplicationPolicy

The `EvaluateAllPolicies` Windows Management Instrumentation (WMI) class method in Configuration Manager that evaluated all policies.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 EvaluateAllPolicies
{
    [IN]    Boolean IsEnforceAction
    [OUT]   String JobIdUser
    [OUT]   String JobIdMachine
};
```

## Parameters

`IsEnforceAction` Data type: `Boolean`

Qualifiers: [id("0"), in]

`True` if the action is enforced.

`JobIdUser` Data type: `String`

Qualifiers: [id("1"), out]

Job identifier of a user policy.

`JobIdMachine` Data type: `String`

Qualifiers: [id("2"), out]

Job identifier of a machine policy.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
