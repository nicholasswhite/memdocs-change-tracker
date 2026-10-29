---
title: "SMS_AzureServicesTask server WMI class"
description: An SMS Provider server class that represents a Microsoft Azure specific operation that can be performed on the specified Microsoft Azure service. This class can be used to initiate an operation and monitor the results of the operation.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68ec7f3a-2bc6-459f-b959-19beb729907d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/90370425-aca4-4a39-9533-d52e5e002a5d
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_AzureServicesTask server WMI class

The `SMS_AzureServicesTask` WMI class is an SMS Provider server class in Configuration Manager, that represents a Microsoft Azure specific operation that can be performed on the specified Microsoft Azure service. This can be used to initiate an operation and monitor the results of the operation.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AzureServicesTask : SMS_BaseClass
{
    UInt32 AzureServiceId;
    String SiteCode;
    DateTime TaskCreationTime;
    DateTime TaskEndTime;
    UInt32 TaskID;
    String TaskKeyValue;
    UInt32 TaskStateId;
    UInt32 TaskTypeId;
    UInt32 Type;
};
```

## Methods

The `SMS_AzureServicesTask` class doesn't define any methods.

## Properties

`AzureServiceId` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

The service identifier key for the `SMS_AzureService` instance on which the current task will be performed.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: none

Site code of the site that owns the task.

`TaskCreationTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Time the task was created.

`TaskEndTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Time the task ended.

`TaskID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key, not_null]

Identifier of the Microsoft Azure service task.

`TaskKeyValue` Data type: `String`

Access type: Read/Write

Qualifiers: none

Input for the task - if necessary. This value isn't needed for `CreateDeployment`, `UpgradeDeployment`, `DeleteDeployment`, `StopDeployment`, or `StartDeployment` and any value will be ignored.

`TaskStateId` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [values]

Identifier of the current task state. Possible values are:

| Value | Task state |
| --- | --- |
| 1 | Created |
| 2 | In Progress |
| 3 | Completed |
| 4 | Failed |

`TaskTypeId` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [not_null, values]

Identifier for type of task. Possible values are:

| Value | Task type |
| --- | --- |
| 1 | CreateDeployment |
| 2 | UpgradeDeployment |
| 3 | DeleteDeployment |
| 4 | StopDeployment |
| 5 | StartDeployment |

`Type` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Type of task. Possible values are:

| Value | Task type |
| --- | --- |
| 0 | RunOnce |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
