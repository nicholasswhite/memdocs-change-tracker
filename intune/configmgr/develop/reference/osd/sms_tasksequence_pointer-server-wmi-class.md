---
title: "SMS_TaskSequence_Pointer Server WMI Class"
description: The SMS_TaskSequence_Pointer WMI class is an SMS provider server class that represents information about an operating system deployment task sequence.
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

# SMS_TaskSequence_Pointer Server WMI Class

The `SMS_TaskSequence_Pointer` Windows Management Instrumentation (WMI) class is an SMS provider server class, in Configuration Manager, that represents information about an operating system deployment task sequence.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_Pointer : SMS_TaskSequence_Step
{
    SMS_TaskSequence_Condition Condition;
    Boolean ContinueOnError;
    String Description;
    Boolean Enabled;
    String Name;
    String SupportedEnvironment;
};

```

## Methods

The `SMS_TaskSequence_Pointer` class does not define any methods.

## Properties

`Condition` Data type: `SMS_TaskSequence_Condition`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md).

`ContinueOnError` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md).

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: [AllowedLen("0-255")]

See [SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md).

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md).

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [AllowedLen("1-100")]

See [SMS_TaskSequence_Step Server WMI Class](sms_tasksequence_step-server-wmi-class.md).

`SupportedEnvironment` Data type: `String`

Access type: Read/Write

Qualifiers: [ValueMap, Not_Null:ToInstance]

The supported environment. The default value is WinPEandFullOS. Possible values are:

| Value |
| --- |
| WinPE |
| FullOS |
| WinPEandFullOS |

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
