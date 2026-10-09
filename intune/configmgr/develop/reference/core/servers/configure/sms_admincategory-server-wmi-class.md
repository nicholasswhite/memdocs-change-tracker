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
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
