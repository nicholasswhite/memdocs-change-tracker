---
description: Learn how the SMS_DPGroupDistributionStatus Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that describes distribution information for a given distribution point group.
title: "SMS_DPGroupDistributionStatus Server WMI Class"
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

# SMS_DPGroupDistributionStatus Server WMI Class

The `SMS_DPGroupDistributionStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that describes distribution information for a given distribution point group.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DPGroupDistributionStatus : SMS_BaseClass
{
    UInt32 Assets;
    UInt32 ContentCount;
    String GroupID;
    UInt32 MessageCategory;
    UInt32 MessageType;
    DateTime StatusTime;
};
```

## Methods

The `SMS_DPGroupDistributionStatus` class doesn't define any methods.

## Properties

`Assets` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of distribution points.

`ContentCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of packages or applications distributed to this distribution point group.

`GroupID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique identifier for the distribution point group.

`MessageCategory` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Status message category.

`MessageType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

See [SMS_StatusMessage Server WMI Class](../manage/sms_statusmessage-server-wmi-class.md).

`StatusTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date and time, in Universal Coordinated Time (UTC), when the status message was created.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
