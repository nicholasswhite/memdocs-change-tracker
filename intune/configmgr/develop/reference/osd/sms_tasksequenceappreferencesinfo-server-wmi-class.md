---
description: Learn how to represent a Configuration Manager application in the task sequence using SMS_TaskSequenceAppReferencesInfo class.
title: "SMS_TaskSequenceAppReferencesInfo Server WMI Class"
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

# SMS_TaskSequenceAppReferencesInfo Server WMI Class

The `SMS_TaskSequenceAppReferencesInfo` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a Configuration Manager application in the task sequence.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequenceAppReferencesInfo : SMS_BaseClass
{
    String PackageID;
    SInt32 RefAppCI_ID;
    String RefAppModelName;
    String RefAppPackageID;
};
```

## Methods

The `SMS_TaskSequenceAppReferencesInfo` class does not define any methods.

## Properties

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Package ID of the task sequence.

`RefAppCI_ID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

CI_ID of the referenced by task sequence application.

`RefAppModelName` Data type: `String`

Access type: Read/Write

Qualifiers: none

The model name of the referenced by task sequence application.

`RefAppPackageID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Package ID of the referenced by task sequence application.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
