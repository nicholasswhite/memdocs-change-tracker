---
description: The SMS_AppFailedVEsData Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.
title: "SMS_AppFailedVEsData Server WMI Class"
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

# SMS_AppFailedVEsData Server WMI Class

The `SMS_AppFailedVEsData` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AppFailedVEsData : SMS_BaseClass
{
    UInt32 AssignmentID;
    String AssignmentUniqueID;
    String CollectionID;
    UInt32 ComplianceState;
    UInt32 DTCI;
    UInt64 DTResultID;
    UInt32 EnforcementState;
    UInt32 ErrorValue;
    String MachineName;
    String UserName;
    String VEDisplayName;
};
```

## Methods

The `SMS_AppFailedVEsData` class does not define any methods.

## Properties

`AssignmentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

AssignmentID

`AssignmentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

AssignmentUniqueID

`CollectionID` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

CollectionID

`ComplianceState` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

ComplianceState

`DTCI` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

DTCI

`DTResultID` Data type: `UInt64`

Access type: Read-only

Qualifiers: [not_null, read]

DTResultID

`EnforcementState` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

EnforcementState

`ErrorValue` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

ErrorValue

`MachineName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

MachineName

`UserName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

UserName

`VEDisplayName` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

VEDisplayName

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
