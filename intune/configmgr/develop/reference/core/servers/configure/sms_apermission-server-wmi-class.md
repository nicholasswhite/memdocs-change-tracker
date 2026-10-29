---
description: Learn how to describe the permission granted to a specific admin in Configuration Manager using SMS_APermission class.
title: "SMS_APermission Server WMI Class"
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

# SMS_APermission Server WMI Class

The `SMS_APermission` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that is embedded by `SMS_Admin` and describes the permission granted to a specific admin.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_APermission :
{
    String CategoryID;
    String CategoryName;
    UInt32 CategoryTypeID;
    String RoleID;
    String RoleName;
};
```

## Methods

The `SMS_APermission` class does not define any methods.

## Properties

`CategoryID` Data type: `String`

Access type: Read/Write

Qualifiers: None

ID of the associated RBA security category or collection.

`CategoryName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the RBA security category or collection.

`CategoryTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [enumeration]

The type of category. The default value is 29.

| Value | Category type |
| --- | --- |
| 1 | Collection |
| 29 | SecuredScope |

`RoleID` Data type: `String`

Access type: Read/Write

Qualifiers: None

ID of the security role.

`RoleName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the role.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
