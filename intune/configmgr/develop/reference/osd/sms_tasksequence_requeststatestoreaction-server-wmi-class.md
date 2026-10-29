---
title: "SMS_TaskSequence_RequestStateStoreAction Server WMI Class"
description: The SMS_TaskSequence_RequestStateStoreAction class represents a task sequence action that requests access to a state migration point when capturing a state from a computer or restoring a state to a computer.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_TaskSequence_RequestStateStoreAction Server WMI Class

The `SMS_TaskSequence_RequestStateStoreAction` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a task sequence action that requests access to a state migration point when capturing a state from a computer or restoring a state to a computer.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_RequestStateStoreAction : SMS_TaskSequence_Action
{
      SMS_TaskSequence_Condition Condition;
      Boolean ContinueOnError;
      String Description;
      Boolean Enabled;
      Boolean FallbackToNAA;
      String Name;
      String RequestType;
      UInt32 SMPRetryCount;
      UInt32 SMPRetryTime;
      String SupportedEnvironment;
      UInt32 Timeout;
};
```

## Methods

The `SMS_TaskSequence_RequestStateStoreAction` class does not define any methods.

## Properties

`Condition` Data type: `SMS_TaskSequence_Condition`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`ContinueOnError` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: [AllowedLen("0-255")]

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`FallbackToNAA` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

`true` if the action should use the network access account (NAA) as a fallback when the computer account fails to connect to the state migration point. The default value is `false`.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [AllowedLen("1-100")]

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`RequestType` Data type: `String`

Access type: Read/Write

Qualifiers: [CommandLineArg(1), Not_Null]

Type of state migration point (SMP) request. Possible values are:

- capture
- restore

  `SMPRetryCount` Data type: `UInt32`

  Access type: Read/Write

  Qualifiers: [Global, ValueRange("0-30")]

  The number of times that the action should try to find a state migration point before failing (global setting). The value must be between 0 and 30.

  `SMPRetryTime` Data type: `UInt32`

  Access type: Read/Write

  Qualifiers: [Global, ValueRange("0-600")]

  The time, in seconds, that the action should wait between retry attempts (global setting).The value must be between 0 and 600.

  `SupportedEnvironment` Data type: `String`

  Access type: Read/Write

  Qualifiers: [Not_Null:ToInstance]

  See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

  The default value of this property for this task sequence action is FullOS.

  `Timeout` Data type: `UInt32`

  Access type: Read/Write

  Qualifiers: None

  See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

## Remarks

Class qualifiers for this class include:

[CommandLine("osdsmpclient.exe /%1"),VariablePrefix("OSDState"),

ActionCategory("UserState,1,4"),ActionUI{"AdminUI.TaskSequenceEditor.dll", "Microsoft.ConfigurationManagement.AdminConsole.TaskSequenceEditor", "RequestStateStoreControl", "TaskSequenceOptionControl"}]

For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
