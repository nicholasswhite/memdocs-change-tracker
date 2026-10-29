---
description: Learn how to use SMS_RbacSecuredObject class, in Configuration Manager, that represents the RBAC Security Object.
title: "SMS_RbacSecuredObject Server WMI Class"
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

# SMS_RbacSecuredObject Server WMI Class

The `SMS_RbacSecuredObject` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the RBAC Security Object.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_RbacSecuredObject : SMS_BaseClass
{
    UInt32 AvailableInstanceOperations;
    UInt32 AvailableTypeOperations;
    UInt32 GrantedOperations;
    UInt32 ObjectTypeID;
    String ObjectTypeName;
    SMS_Operation Operations[];
};
```

## Methods

The following table lists the methods in the `SMS_RbacSecuredObject` class.

| Method | Description |
| --- | --- |
| [UserHasPermissions Method in Class SMS_RbacSecuredObject](userhaspermissions-method-in-class-sms_rbacsecuredobject.md) | Returns `true` if the current user has all the requested rights to the given object. |
| [GetCollectionsWithResourcePermissions Method in Class SMS_RbacSecuredObject](getcollectionswithresourcepermissions-method-in-class-sms_rbacsecuredobject.md) | Retrieves the collections that the given resource is a member of and the requested permissions. |
| [GetAvailableScopes Method in Class SMS_RbacSecuredObject](getavailablescopes-method-in-class-sms_rbacsecuredobject.md) | Returns the secured scopes which current user has all the specified roles associated. |
| [GetUserList Method in Class SMS_RbacSecuredObject](getuserlist-method-in-class-sms_rbacsecuredobject.md) | Returns the secured scopes which current user has all the specified roles associated. |

## Properties

`AvailableInstanceOperations` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Available instance level permissions. Detail at Operations.

`AvailableTypeOperations` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Available permissions. Detail at Operations.

`GrantedOperations` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The operations which are granted to the current user for this type of object.

`ObjectTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The type of object.

`ObjectTypeName` Data type: `String`

Access type: Read/Write

Qualifiers: [sizelimit("256")]

Name of the object type.

`Operations` Data type: `SMS_Operation` Array

Access type: Read/Write

Qualifiers: [lazy]

The list of operations which belong to this type.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
