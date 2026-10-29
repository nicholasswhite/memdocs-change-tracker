---
title: "CCM_CIEvaluationJob Client WMI Class"
description: The CCM_CIEvaluationJob Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a configuration item evaluation job.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CCM_CIEvaluationJob Client WMI Class

The `CCM_CIEvaluationJob` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a configuration item evaluation job.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_CIEvaluationJob :
{
    String CIAgentJobId;
    UInt32 ErrorCode;
    String Id;
    Boolean IsMachineTarget;
    Boolean IsRebootRequired;
    String JobState;
    DateTime LastModifiedTime;
    String OwnerSID;
    String Type;
    String UserSID;
};
```

## Methods

The `CCM_CIEvaluationJob` class doesn't define any methods.

## Properties

`CIAgentJobId` Data type: `String`

Access type: Read/Write

Qualifiers: none

CI agent job identifier.

`ErrorCode` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Error code.

`Id` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier.

`IsMachineTarget` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if this is a device targeted application.

`IsRebootRequired` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if a reboot is required.

`JobState` Data type: `String`

Access type: Read/Write

Qualifiers: [values]

Job state. Possible values are:

| Value |
| --- |
| Idle |
| Evaluating |
| Success |
| Error |
| CanceledOrDeleted |

`LastModifiedTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Last modified time.

`OwnerSID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Owner identifier (SID).

`Type` Data type: `String`

Access type: Read/Write

Qualifiers: [valuemap]

Job type. Possible values are:

| Value |
| --- |
| DesiredConfiguration |
| ApplicationManagement |
| SoftwareUpdates |

`UserSID` Data type: `String`

Access type: Read/Write

Qualifiers: none

User identifier (SID).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
