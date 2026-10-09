---
description: Learn how to represent a policy condition in Configuration Manager using CCM_Policy_Condition.
title: "CCM_Policy_Condition Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
---

# CCM_Policy_Condition Client WMI Class

In Configuration Manager, the `CCM_Policy_Condition` class is a client Windows Management Instrumentation (WMI) class that represents a policy condition.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Policy_Condition : CCM_Policy_Config
{
      String ConditionID;
      Boolean ConditionState;
      Object ConditionExpression;
};
```

## Properties

`ConditionID` Data type: `Boolean`

Access type: Read-only

Qualifiers: [key]

Condition ID.

`ConditionState` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

Current state of the condition. This value indicates the result of the last condition evaluation, or it is `null` if the condition has never been evaluated.

`ConditionExpression` Data type: `Object`

Access type: Read-only

Qualifiers: [read]

Actual expression to evaluate. The value is a [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md) object for a simple expression or a [CCM_Policy_Operator Client WMI Class](ccm_policy_operator-client-wmi-class.md) object for a compound expression.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Policy Agent Client WMI Classes](policy-agent-client-wmi-classes.md) [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md) [CCM_Policy_Operator Client WMI Class](ccm_policy_operator-client-wmi-class.md)
