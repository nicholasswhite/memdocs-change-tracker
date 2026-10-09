---
title: "SMS_SiteControlDaySchedule Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents usage information for each hour of the day.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aebdc4a3-c54b-4eea-94e3-663d5e166f57
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/1baec8e6-ab38-4b56-bb59-f6282d94f311
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# SMS_SiteControlDaySchedule Server WMI Class

The `SMS_SiteControlDaySchedule` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents usage information for each hour of the day.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SiteControlDaySchedule
{
     Boolean Backup[24];
     UInt32 HourUsage[24];
     Boolean update;
};
```

## Methods

The `SMS_SiteControlDaySchedule` class does not define any methods.

## Properties

`Backup` Data type: `Boolean` Array

Access type: Read/Write

Qualifiers: None

Array containing 24 elements, one for each hour of the day. A value of `true` indicates that the address (sender) embedding `SMS_SiteControlDaySchedule` can be used as a backup.

`HourUsage` Data type: `UInt32` Array

Access type: Read/Write

Array containing 24 elements, one for each hour of the day. This property specifies the type of usage for each hour. Possible values are:

| Value | Usage type |
| --- | --- |
| 1 | ALL_PRIORITY |
| 2 | ALL_BUT_LOW |
| 3 | HIGH_ONLY |
| 4 | CLOSED |

`update` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

`true` if the usage data is saved when the parent address object is saved.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SCI_Address Server WMI Class](sms_sci_address-server-wmi-class.md)
