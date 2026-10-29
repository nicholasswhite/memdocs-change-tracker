---
description: Learn how to create an abstract base class representing operating system extended history for a client computer using SMS_G_System_ExtHistory.
title: "SMS_G_System_ExtHistory Server WMI Class"
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

# SMS_G_System_ExtHistory Server WMI Class

The `SMS_G_System_ExtHistory` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that serves as an abstract base class representing operating system extended history for a client computer.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_G_System_ExtHistory : SMS_G_System
{
     UInt32 GroupID;
     UInt32 ResourceID;
     UInt32 RevisionID;
     DateTime TimeStamp;
};
```

## Methods

The `SMS_G_System_ExtHistory` class does not define any methods.

## Properties

`GroupID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

ID of the group that distinguishes one hardware inventory instance from another within one client resource. For example, each logical disk object for a client is assigned a unique `GroupID` value.

`ResourceID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

See [SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md).

`RevisionID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

ID that increments if the object changes after the last time inventory was taken. The highest number indicates the most recent update. Objects with the same `ResourceID` and `GroupID` values are deltas. They differ from one another by the `RevisionID` number.

`TimeStamp` Data type: `DateTime`

Access type: Read-only

Qualifiers: None

Date and time of the inventory.

## Remarks

Your application uses this class to determine the state of a client at any given time. Names of derived extended history classes are prefixed with "SMS_GEH_System_" followed by the inventoried object name. An example class name is `SMS_GEH_System_ACCOUNT`. Your application can use the derived classes to determine the state of a hardware component on a client at a given point in time.

The SMS Provider determines the state by using the information from classes derived from both [SMS_G_System_Current Server WMI Class](sms_g_system_current-server-wmi-class.md) and [SMS_G_System_History Server WMI Class](sms_g_system_history-server-wmi-class.md). However, the application cannot query `SMS_G_System_ExtHistory` to determine the state of all hardware components on a client at a given point in time.

Your query must include the `ResourceID` and `TimeStamp` values in the WHERE clause, as shown in the following example.

```
SELECT * FROM SMS_GEH_System_Logical_Disk
WHERE ResourceID = <resourceid>
AND Timestamp = "<timestamp>"
```

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md)
