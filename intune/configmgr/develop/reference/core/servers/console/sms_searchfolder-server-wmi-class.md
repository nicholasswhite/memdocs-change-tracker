---
description: Learn how to use SMS_SearchFolder WMI class in Configuration Manager to perform search operations.
title: "SMS_SearchFolder Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/12ed19f9-ebdf-4c8a-8bcd-7a681836774d
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3a764584-4f97-452b-8f1d-36f19b12f6ae
---

# SMS_SearchFolder Server WMI Class

The `SMS_SearchFolder` WMI class is an SMS Provider server class, in Configuration Manager, that behaves the same as `SMS_ObjectContainerNode`, but is only used for search operations.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SearchFolder : SMS_BaseClass
{
   UInt32 FolderId;
   String GroupID;
   Boolean IsSystem;
   String Name;
   UInt32 ObjectType;
   String SearchString;
   String SourceSite;
};
```

## Methods

The `SMS_SearchFolder` class does not define any methods.

## Properties

`FolderId` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The unique ID of this search folder.

`GroupID` Data type: `String`

Access type: Read/Write

Qualifiers: None

The Group ID of the search folder.

`IsSystem` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read, not_null]

A flag that indicates whether this is a system folder.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

Folder name. Default value is New Folder.

`ObjectType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The type of the folder.

`SearchString` Data type: `String`

Access type: Read/Write

Qualifiers: None

Search string get/set by AdminConsole.

`SourceSite` Data type: `String`

Access type: Read-only

Qualifiers: [read, not_null]

The sidecode of the site that the folder originated from.

## Remarks

In Configuration Manager, the search folder and folders were one class. Now, in Configuration Manager, they are separate classes. `SMS_SearchFolders` folders appear in the "Manage Searches" class of menus in the console. The `SMS_SearchFolders` folders have no dedicated node and are used for node searches only. `SMS_SearchFolders` folders cannot be used for global searches.

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers that are included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_ObjectContainerItem Server WMI Class](sms_objectcontaineritem-server-wmi-class.md)
