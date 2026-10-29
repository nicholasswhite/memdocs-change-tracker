---
title: "SMS_CollectionPermission Server WMI Class"
description: Article outlining the use of SMS_CollectionPermission in Configuration Manager to query and define which collection scopes are associated to an RBAC role.
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

# SMS_CollectionPermission Server WMI Class

The `SMS_CollectionPermission` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, is used to query and define which collection scopes are associated to an RBAC role.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CollectionPermission : SMS_BaseClass
{
      UInt32 AdminID;
      String CollectionID;
      String CollectionName;
      Boolean GrantedToCurrentUser;
      String LogonName;
      String RoleID;
      String RoleName;
};
```

## Methods

The `SMS_ CollectionPermission` class does not define any methods.

## Properties

`AdminID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The administrator id from RBAC, which is used to associate the collection between each instance of this class.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The ID that refers to the collection.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: None

The name of the collection.

`GrantedToCurrentUser` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

This value will be true if this permission is granted to the current user directly or indirectly (through a Security Group).

`LogonName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Name of the resource.

`RoleID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The role id from RBAC, which is used to associate the collection between each instance of this class.

`RoleName` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The name of the RBAC.

## Remarks

Class qualifiers for this class include:

- Abstract

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
