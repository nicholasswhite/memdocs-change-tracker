---
description: Learn how to represent an association between the admin account and an RBA secured category in Configuration Manager using SMS_AdminCategory.
title: "SMS_AdminCategory Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_AdminCategory Server WMI Class

The `SMS_AdminCategory` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents an association between the admin account and an RBA secured category.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AdminCategory : SMS_BaseClass
{
    UInt32 AdminID;
    String CategoryID;
};
```

## Methods

The `SMS_AdminCategory` class does not define any methods.

## Properties

`AdminID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

ID of the associated account.

`CategoryID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID of the associated RBA secured category.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
