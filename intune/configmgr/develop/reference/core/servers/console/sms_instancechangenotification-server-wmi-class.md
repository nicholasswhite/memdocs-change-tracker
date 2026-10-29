---
description: Learn how to notify the administrator console that an alert has changed its status with SMS_InstanceChangeNotification class.
title: "SMS_InstanceChangeNotification Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_InstanceChangeNotification Server WMI Class

The `SMS_InstanceChangeNotification` WMI class is an SMS Provider server class, in Configuration Manager, that notifies the administrator console that an alert has changed its status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_InstanceChangeNotification : SMS_BaseClass
{
   String Action;
   String ClassName;
   ref:SMS_BaseClass InstancePath;
   UInt8[] SECURITY_DESCRIPTOR;
   UInt64 TIME_CREATED;
};
```

## Methods

The `SMS_InstanceChangeNotification` class does not define any methods.

## Properties

`Action` Data type: `String`

Access type: Read/Write

Qualifiers: None

The action that caused the change notification.

| Possible values |
| --- |
| Insert |
| Update |
| Delete |

`ClassName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Name of the class that caused the change notification. For example, for an alert, the name of the class is SMS_Alert.

`InstancePath` Data type: `ref:SMS_BaseClass`

Access type: Read/Write

Qualifiers: None

The instance path of the object that caused the change notification.

`SECURITY_DESCRIPTOR` Data type: `UInt8[]`

Access type: Read/Write

Qualifiers: None

For internal use only.

`TIME_CREATED` Data type: `UInt64`

Access type: Read/Write

Qualifiers: None

For internal use only.

## Remarks

This class allows alert tiles to be updated with the most recent status information.

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers that are included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
