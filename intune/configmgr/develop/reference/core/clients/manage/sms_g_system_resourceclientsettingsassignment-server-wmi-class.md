---
description: Learn how to represent resource-specific client agent settings assignments in Configuration Manager.
title: "SMS_G_SYSTEM_ResourceClientSettingsAssignment Server WMI Class"
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

# SMS_G_SYSTEM_ResourceClientSettingsAssignment Server WMI Class

The `SMS_G_System_ResourceClientSettingsAssignment` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents resource-specific (device or user) client agent settings assignments.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_G_System_ResourceClientSettingsAssignment : SMS_G_System
{
     String AssignmentUniqueID;
     String CollectionName;
     UInt32 ID;
     String Name;
     UInt32 Priority;
     String UniqueID;
     UInt32 ResourceID;
     UInt32 Type;
};
```

## Methods

The `SMS_G_System_ResourceClientSettingsAssignment` class does not define any methods.

## Properties

`AssignmentUniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Assignment Unique ID.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Name of the collection.

`ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Identifier.

`Priority` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Identifier.

`UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: None

Unique identifier for the settings.

`ResourceID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

See [SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md).

`Type` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

Settings type. Possible values are:

| Value | Settings type |
| --- | --- |
| 1 | Device |
| 2 | User |

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
