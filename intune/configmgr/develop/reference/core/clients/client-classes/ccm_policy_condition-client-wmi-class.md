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
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
