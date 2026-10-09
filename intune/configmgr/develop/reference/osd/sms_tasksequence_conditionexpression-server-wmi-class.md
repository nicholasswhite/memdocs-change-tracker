---
title: "SMS_TaskSequence_ConditionExpression Server WMI Class"
description: The SMS_TaskSequence_ConditionExpression WMI class is an SMS Provider server class that is the abstract base class for all condition expressions.
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

# SMS_TaskSequence_ConditionExpression Server WMI Class

The `SMS_TaskSequence_ConditionExpression` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that is the abstract base class for all condition expressions.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_ConditionExpression : SMS_TaskSequence_ConditionOperand
{
};
```

## Methods

The `SMS_TaskSequence_ConditionExpression` class does not define any methods.

## Properties

The `SMS_TaskSequence_ConditionExpression` class does not define any properties.

## Remarks

Class qualifiers for this class include:

- Abstract

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  `SMS_TaskSequence_ConditionExpression` is the abstract base class for an expression that must evaluate to `true`, for the task sequence step to be processed. For example, the derived class [SMS_TaskSequence_RegistryConditionExpression Server WMI Class](sms_tasksequence_registryconditionexpression-server-wmi-class.md) defines an expression for the existence of a registry key.

  An `SMS_TaskSequence_ConditionExpression` is stored in a condition's ([SMS_TaskSequence_Condition Server WMI Class](sms_tasksequence_condition-server-wmi-class.md)) `Operands` array property, which defines the list of condition operands.

> [!NOTE]
>
> In a task sequence step ([SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md)), the condition is defined in the `Condition` property.

Alternatively, more complex conditions are created by adding a [SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md) object to the condition's `Operands` array property, and by adding expressions and operators to the added [SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md)`Operands` array.

For more information, see Operating System Deployment Task Sequence Object Model.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md) [SMS_TaskSequence_Condition Server WMI Class](sms_tasksequence_condition-server-wmi-class.md) [SMS_TaskSequence_ConditionOperand Server WMI Class](sms_tasksequence_conditionoperand-server-wmi-class.md)
