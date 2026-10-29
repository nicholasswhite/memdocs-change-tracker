---
description: Learn how to track the history of a request each time a request is updated using SMS_VirtualEnvironment in Configuration Manager.
title: "SMS_VirtualEnvironment Server WMI Classes"
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

# SMS_VirtualEnvironment Server WMI Classes

The `SMS_VirtualEnvironment` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_UserApplicationRequestHistoryItem :
{
    boolean IsReadOnly;;
    SMS_CI_LocalizedProperties LocalizedInformation[];
    uint32 NumReferringApplications;
    uint32 NumReferringDeploymentTypes;
    uint32 ReferringDeploymentTypes[];
};
```

## Methods

The `SMS_UserApplicationRequestHistoryItem` class does not define any methods.

## Properties

`IsReadOnly` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Flag to indicate the virtual environment is read-only.

`LocalizedInformation` Data type: `SMS_CI_LocalizedProperties` Array

Access type: Read/Write

Qualifiers: [lazy]

Localized information.

`NumReferringApplications` Data type: `UInt32`

Access type: Read

Qualifiers: [read, not_null]

The number of referring applications.

`NumReferringDeploymentTypes` Data type: `UInt32`

Access type: Read

Qualifiers: [read, not_null]

The number of referring deployment types.

`ReferringDeploymentTypes` Data type: `UInt32` Array

Access type: Read/Write

Qualifiers: [lazy]

A list of CI_IDs of the referring deployment types.

## Remarks

## Requirements

Each time a request is updated, an instance of this class is created to track the history of the request.

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
