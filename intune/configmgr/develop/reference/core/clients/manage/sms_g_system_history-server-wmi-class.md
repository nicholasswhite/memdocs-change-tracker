---
title: "SMS_G_System_History Server WMI Class"
description: The SMS_G_System_History class is an SMS Provider server class that serves as an abstract base class representing hardware component state history for a client computer.
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

# SMS_G_System_History Server WMI Class

The `SMS_G_System_History` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that serves as an abstract base class representing hardware component state history for a client computer.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_G_System_History : SMS_G_System
{
     UInt32 GroupID;
     UInt32 ResourceID;
     UInt32 RevisionID;
     DateTime TimeStamp;
};
```

## Methods

The `SMS_G_System_History` class does not define any methods.

## Properties

`GroupID` Data type: **UInt32**

Access type: Read-only

Qualifiers: [key]

ID of the group that distinguishes one hardware inventory instance from another within one client resource. For example, each logical disk object for a client is assigned a unique `GroupID` value.

`ResourceID` Data type: **UInt32**

Access type: Read/Write

Qualifiers: [key]

See [SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md).

`RevisionID` Data type: **UInt32**

Access type: Read-only

Qualifiers: [key]

ID that increments if the object changes after the last time inventory was taken. The highest number indicates the most recent update. Objects with the same `ResourceID` and `GroupID` values are deltas. They differ from one another by the `RevisionID` number.

`TimeStamp` Data type: **DateTime**

Access type: Read-only

Qualifiers: None

Date and time of the inventory.

## Remarks

History objects are created from the current hardware component object when the component has changed since the last inventory. This class represents a collection of prior hardware component states for the client.

Your application uses this class to determine the state of client hardware at any given time. Names of derived history classes are prefixed with "SMS_GEH_System_" followed by the inventoried object name. An example class name is `SMS_GEH_System_ACCOUNT`. Your application can use the derived classes to determine the state of a hardware component on a client at a given point in time.

Hardware history is deleted on a schedule if the Delete Aged Inventory History database maintenance task is set to `true` in the Configuration Manager console. You can also enable this task and set the schedule by updating the site control file. The site control item [SMS_SCI_SQLTask Server WMI Class](../../servers/configure/sms_sci_sqltask-server-wmi-class.md) object, and the `TaskName` value is "Delete Aged Inventory History". For an example that updates the site control file, see [About the site control file](../../../../core/understand/about-the-configuration-manager-site-control-file.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md)
