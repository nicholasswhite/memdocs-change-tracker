---
description: Learn how to store a compound expression that evaluates to either true or false in Configuration Manager using CCM_Policy_Operator.
title: "CCM_Policy_Operator Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
---

# CCM_Policy_Operator Client WMI Class

In Configuration Manager, the `CCM_Policy_Operator` class is a client Windows Management Instrumentation (WMI) class that stores a compound expression that evaluates to either `true` or `false`.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
class CCM_Policy_Operator : CCM_Policy_Config
{
      String OperatorType;
   Object Operands[];
};
```

## Properties

`OperatorType` Data type: `String`

Access type: Read-only

Qualifier: [Not_Null:ToInstance]

The type of operator. Possible values are:

| Value | Description |
| --- | --- |
| `AND` | A logical `AND` operator. The result of the compound expression is only `true` if all of its operands evaluate to `true`. |
| `OR` | A logical `OR` operator. The result of the compound expression is `true` if any one of its operands evaluates to `true`. |
| `NOT` | A logical `NOT` operator. This operator can only have a single operand. The result of the expression is `true` only if the operand evaluates to `false`. |

`Operands` Data type: `Object`

Access type: Read-only

Qualifier: [Not_Null:ToInstance]

Operands for the compound expression. Each operand can be a [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md) object or a `CCM_Policy_Operator` object if further nesting is required.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Policy Agent Client WMI Classes](policy-agent-client-wmi-classes.md) [CCM_Policy_Expression Client WMI Class](ccm_policy_expression-client-wmi-class.md)
