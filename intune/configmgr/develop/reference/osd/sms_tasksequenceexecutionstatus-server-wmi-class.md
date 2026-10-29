---
title: "SMS_TaskSequenceExecutionStatus Server WMI Class"
description: In Configuration Manager, The SMS_TaskSequenceExecutionStatus WMI class is an SMS Provider server class that represents the status of an execution of a task sequence.
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

# SMS_TaskSequenceExecutionStatus Server WMI Class

The `SMS_TaskSequenceExecutionStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the status of an execution of a task sequence.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequenceExecutionStatus : SMS_BaseClass
{
    String ActionName;
    String ActionOutput;
    String AdvertisementID;
    DateTime ExecutionTime;
    UInt32 ExitCode;
    String GroupName;
    UInt32 LastStatusMsgID;
    String LastStatusMsgName;
    String PackageID;
    UInt32 ResourceID;
    UInt32 Step;
};
```

## Methods

The `SMS_TaskSequenceExecutionStatus` class does not define any methods.

## Properties

`ActionName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the action in the task sequence that was executed.

`ActionOutput` Data type: `String`

Access type: Read/Write

Qualifiers: none

Console output of the task sequence step that was executed.

`AdvertisementID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Deployment identifier of the task sequence.

`ExecutionTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: [key]

Run time of the task sequence.

`ExitCode` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Exit code of the task sequence step that was executed.

`GroupName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Group name in the task sequence that was executed.

`LastStatusMsgID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Identifier for this execution status.

`LastStatusMsgName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name for this execution status.

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Task sequence package identifier.

`ResourceID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Client computer identifier.

`Step` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Step number in the task sequence that was executed.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
