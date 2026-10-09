---
title: "SMS_TaskSequence_ConvertDiskAction Server WMI Class"
description: In Configuration Manager, the SMS_TaskSequence_ConvertDiskAction Windows Management Instrumentation class is an SMS Provider server class that represents a task sequence action that converts a physical disk from a basic disk type to a dynamic disk type.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68cb9039-df60-49b0-8ef8-89ad96497f63
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/725b6df3-93e8-472d-834e-e7e0d2953d35
---

# SMS_TaskSequence_ConvertDiskAction Server WMI Class

The `SMS_TaskSequence_ConvertDiskAction` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a task sequence action that converts a physical disk from a basic disk type to a dynamic disk type.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_ConvertDiskAction : SMS_TaskSequence_Action
{
      SMS_TaskSequence_Condition Condition;
      Boolean ContinueOnError;
      String Description;
      UInt32 DiskIndex;
      Boolean Enabled;
      String Name;
      String SupportedEnvironment;
      UInt32 Timeout;
};
```

## Methods

The `SMS_TaskSequence_ConvertDiskAction` class does not define any methods.

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

`DiskIndex` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Not_Null, VariableName("OSDConvertDiskIndex")]

The physical disk number to convert.

The task sequence variable associated with this property is OSDConvertDiskIndex. For more information, see [OS deployment task sequence variables](../../../osd/understand/task-sequence-variables.md).

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [AllowedLen("1-100")]

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`SupportedEnvironment` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null:ToInstance]

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

`Timeout` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Action Server WMI Class](sms_tasksequence_action-server-wmi-class.md).

## Remarks

Class qualifiers for this class include:

[CommandLine("osddiskpart.exe convert %%OSDConvertDiskIndex%%"),

VariablePrefix("OSD"),ActionCategory{"Disks,2,3"},

ActionUI{"AdminUI.TaskSequenceEditor.dll", "Microsoft.ConfigurationManagement.AdminConsole.TaskSequenceEditor", "ConvertDiskToDynamicControl", "TaskSequenceOptionControl"}]

For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See also

[SMS_TaskSequence_Action server WMI class](sms_tasksequence_action-server-wmi-class.md)
