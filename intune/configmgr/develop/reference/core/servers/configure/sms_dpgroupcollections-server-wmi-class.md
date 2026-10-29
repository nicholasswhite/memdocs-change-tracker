---
title: "SMS_DPGroupCollections Server WMI Class"
description: An SMS Provider server class that describes collection association for a given distribution point group.
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

# SMS_DPGroupCollections Server WMI Class

The `SMS_DPGroupCollections` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that describes collection association for a given distribution point group.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DPGroupCollections : SMS_BaseClass
{
    String CollectionDescription;
    String CollectionID;
    UInt32 CollectionMemberCount;
    String CollectionName;
    String GroupDescription;
    String GroupID;
    String GroupName;
};
```

## Methods

The `SMS_DPGroupCollections` class does not define any methods.

## Properties

`CollectionDescription` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description of the collection.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Collection associated with the distribution point group.

`CollectionMemberCount` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Count of the collection members.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the collection.

`GroupDescription` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description of the distribution point group.

`GroupID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier for the distribution point group.

`GroupName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the distribution point group.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
