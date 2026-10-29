---
title: "SMS_SecuredCategoryMembership Server WMI Class"
description: Learn how to use the SMS_SecuredCategoryMembership class in Configuration Manager.
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

# SMS_SecuredCategoryMembership Server WMI Class

The `SMS_SecuredCategoryMembership` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents object to security category assignment.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SecuredCategoryMembership : SMS_BaseClass
{
    String CategoryID;
    String ObjectKey;
    UInt32 ObjectTypeID;
};
```

## Methods

The following table lists the methods in the `SMS_SecuredCategoryMembership` class.

| Method | Description |
| --- | --- |
| [AddMemberships Method in Class SMS_SecuredCategoryMembership](addmemberships-method-in-class-sms_securedcategorymembership.md) | Batch operation to assign objects to a security category. |
| [RemoveMemberships Method in Class SMS_SecuredCategoryMembership](removememberships-method-in-class-sms_securedcategorymembership.md) | Batch operation to remove objects from a security category |

## Properties

`CategoryID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The ID of security category.

`ObjectKey` Data type: `String`

Access type: Read/Write

Qualifiers: [key, sizelimit("256")]

The key of object.

`ObjectTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The type id of the object. See the `SMS_RbacSecuredObject` class for details.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
