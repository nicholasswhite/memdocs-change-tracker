---
title: "SMS_ObjectContainerItem Server WMI Class"
description: An SMS Provider server class that contains information about a Configuration Manager console folder item.
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

# SMS_ObjectContainerItem Server WMI Class

The `SMS_ObjectContainerItem` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that contains information about a Configuration Manager console folder item.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ObjectContainerItem : SMS_BaseClass
{
    UInt32 ContainerNodeID;
    String InstanceKey;
    String MemberGuid;
    UInt32 MemberID;
    UInt32 ObjectType;
    String ObjectTypeName;
    String SourceSite;
};
```

## Methods

The following table lists the methods in the `SMS_ObjectContainerItem` class.

| Method | Description |
| --- | --- |
| [MoveMembers Method in Class SMS_ObjectContainerItem](movemembers-method-in-class-sms_objectcontaineritem.md) | Moves one or more folder items to another folder. |
| [MoveMembersEx Method in Class SMS_ObjectContainerItem](movemembersex-method-in-class-sms_objectcontaineritem.md) | Moves one or more folder items to another folder. |

## Properties

`ContainerNodeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Not_null]

The unique ID of the folder.

`InstanceKey` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_null]

The name of the folder.

`MemberGuid` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

The guid of the relation.

`MemberID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key, Not_null]

The unique ID of the relation.

`ObjectType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [deprecated, enumeration, read]

The type of the folder. Possible values are listed below.

| Value | Object type |
| --- | --- |
| 2 | TYPE_PACKAGE |
| 3 | TYPE_ADVERTISEMENT |
| 7 | TYPE_QUERY |
| 8 | TYPE_REPORT |
| 9 | TYPE_METEREDPRODUCTRULE |
| 11 | TYPE_CONFIGURATIONITEM |
| 14 | TYPE_OSINSTALLPACKAGE |
| 17 | TYPE_STATEMIGRATION |
| 18 | TYPE_IMAGEPACKAGE |
| 19 | TYPE_BOOTIMAGEPACKAGE |
| 20 | TYPE_TASKSEQUENCEPACKAGE |
| 21 | TYPE_DEVICESETTINGPACKAGE |
| 23 | TYPE_DRIVERPACKAGE |
| 25 | TYPE_DRIVER |
| 1011 | TYPE_SOFTWAREUPDATE |
| 2011 | TYPE_CONFIGURATIONBASELINE |
| 5000 | TYPE_DEVICE_COLLECTION |
| 5001 | TYPE_USER_COLLECTION |

`ObjectTypeName` Data type: `String`

Access type: Read/Write

Qualifiers: None

The WMI Class Name of the object. Example SMS_Package. This will take effect if the ObjectType is 0 or null.

`SourceSite` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

The sitecode of the site that the relation was originally created from.

## Remarks

When attempting to move an item from a root node such as a user collection or device collection, the item doesn't exist as an SMS_ObjectContainerItem. As such a new instance will need to be created instead.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
