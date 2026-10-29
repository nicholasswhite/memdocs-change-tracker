---
title: "SMS_TaskSequence_OSExpressionGroup Server WMI Class"
description: In Configuration Manager, the SMS_TaskSequence_OSExpressionGroup WMI class is an SMS Provider server class that represents an evaluation of a single operating system platform in a task sequence.
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

# SMS_TaskSequence_OSExpressionGroup Server WMI Class

The `SMS_TaskSequence_OSExpressionGroup` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents an evaluation of a single operating system platform in a task sequence. An object of this type is always contained by an [SMS_TaskSequence_OSConditionGroup Server WMI Class](sms_tasksequence_osconditiongroup-server-wmi-class.md) object.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_OSExpressionGroup : SMS_TaskSequence_ConditionOperator
{
      String Name;
      SMS_TaskSequence_WMIConditionExpression Operands[];
      String OperatorType;
      String PlatformArchKey;
      String PlatformMaxVerKey;
      String PlatformMinVerKey;
      String PlatformTypeKey;
};
```

## Methods

The `SMS_TaskSequence_OSExpressionGroup` class does not define any methods.

## Properties

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: None

Optional. The name of an operating system, for example, "Windows XP SP2". The default value is "". See the `DisplayText` property for `SMS_SupportedPlatforms`.

`Operands` Data type: `SMS_TaskSequence_WMIConditionExpression`Array

Access type: Read/Write

Qualifiers: [Not_NULL]

See [SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md).

Each element of this property is an [SMS_TaskSequence_WMIConditionExpression Server WMI Class](sms_tasksequence_wmiconditionexpression-server-wmi-class.md) object that matches the WQL query for the `SMS_SupportedPlatforms` Server WMI Class object indexed by the platform keys. The expressions are typically built from the WQL query stored in the `Condition` property of `SMS_SupportedPlatforms`. There must be at least one [SMS_TaskSequence_WMIConditionExpression Server WMI Class](sms_tasksequence_wmiconditionexpression-server-wmi-class.md) contained by the [SMS_TaskSequence_OSExpressionGroup Server WMI Class](sms_tasksequence_osexpressiongroup-server-wmi-class.md).

`OperatorType` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_NULL]

See [SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md).

The only operator type supported by this class is "and".

`PlatformArchKey` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null]

Platform key that maps to the `OSPlatform` property for `SMS_SupportedPlatforms` objects. For more information, see the Remarks section later in this topic.

`PlatformMaxVerKey` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null]

Platform key that maps to the `OSMaxVersion` property for `SMS_SupportedPlatforms` objects. For more information, see the Remarks section later in this topic.

`PlatformMinVerKey` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null]

Platform key that maps to the `OSMinVersion` property for SMS_SupportedPlatforms objects. For more information, see the Remarks section later in this topic.

`PlatformTypeKey` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null]

Platform key that maps to the `OSName` property for `SMS_SupportedPlatforms` objects. For more information, see the Remarks section later in this topic.

## Remarks

There are no class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

The platform strings specified by `PlatformArchKey`, `PlatformMaxVerKey`, `PlatformMinVerKey`, and `PlatformTypeKey` are used to index the corresponding `SMS_SupportedPlatforms` object instance for the expression.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_TaskSequence_ConditionOperator Server WMI Class](sms_tasksequence_conditionoperator-server-wmi-class.md) [SMS_SupportedPlatforms Server WMI Class](../core/servers/configure/sms_supportedplatforms-server-wmi-class.md) [SMS_TaskSequence_WMIConditionExpression Server WMI Class](sms_tasksequence_wmiconditionexpression-server-wmi-class.md)
