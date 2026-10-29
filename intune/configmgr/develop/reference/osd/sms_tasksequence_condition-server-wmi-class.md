---
title: "SMS_TaskSequence_Condition Server WMI Class"
description: In Configuration Manager, the SMS_TaskSequence_Condition Server WMI Class WMI class is an SMS Provider server class that defines a condition for an operating system deployment step.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_TaskSequence_Condition Server WMI Class

The `SMS_TaskSequence_Condition Server WMI Class` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that defines a condition for an operating system deployment step. This class is the base class for all conditions.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_Condition
{
      SMS_TaskSequence_ConditionOperand Operands[];
};
```

## Methods

The `SMS_TaskSequence_Condition` class does not define any methods.

## Properties

`Operands` Data type: `SMS_TaskSequence_ConditionOperand` Array

Access type: Read/Write

Qualifiers: [Not_Null:ToInstance]

[SMS_TaskSequence_ConditionOperand Server WMI Class](sms_tasksequence_conditionoperand-server-wmi-class.md) objects indicating condition operands. For example, the array can contain a single expression, such as an [SMS_TaskSequence_WMIConditionExpression Server WMI Class](sms_tasksequence_wmiconditionexpression-server-wmi-class.md) object. A more complicated condition array can contain a combination of expressions, operators, and operating system condition groups.

## Remarks

There are no class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

This class is the root for a hierarchy of operator and expression objects that represent the condition that determines whether a step or group or action should be executed. This class implies an AND operator. Therefore, all child operands in the array must be `true` for the overall condition to be `true`.

For example, you might want to process a step on a computer that must have Microsoft Office 2007 and Windows Vista installed. In this case, you add to the `Operands` property array, a [SMS_TaskSequence_SoftwareConditionExpression Server WMI Class](sms_tasksequence_softwareconditionexpression-server-wmi-class.md) that defines Microsoft Office 2007 and a [SMS_TaskSequence_OSConditionGroup Server WMI Class](sms_tasksequence_osconditiongroup-server-wmi-class.md) that defines Windows Vista. The overall condition evaluates to `true` only when the two operands are `true`. That is, when Microsoft Office 2007 is installed on a computer with Windows Vista installed.

For more information about conditions, see Operating System Deployment Task Sequence Object Model.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See also

[SMS_TaskSequence_ConditionOperand Server WMI Class](sms_tasksequence_conditionoperand-server-wmi-class.md) [SMS_TaskSequence_WMIConditionExpression Server WMI Class](sms_tasksequence_wmiconditionexpression-server-wmi-class.md)
