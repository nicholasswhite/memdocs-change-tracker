---
title: "SMS_ImageServicingSchedule Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn about the simplified syntax, methods, properties, and requirements of the SMS_ImageServicingSchedule server class.
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SMS_ImageServicingSchedule Server WMI Class

The `SMS_ImageServicingSchedule` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents schedule details for offline servicing image.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ImageServicingSchedule : SMS_BaseClass
{
    SInt32 Action;
    Boolean ContinueOnError;
    String Description;
    DateTime LastRunDateTime;
    String Name;
    String Schedule;
    SInt32 ScheduleID;
    SInt32 State;
    Boolean UpdateDP;
};
```

## Methods

The `SMS_ImageServicingSchedule` class does not define any methods.

## Properties

`Action` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

Action for software update.

| Value | Update action |
| --- | --- |
| 0 | None. |
| 1 | Install software update immediately. |
| 2 | Cancel software update installation. |

`ContinueOnError` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` to continue to apply software updates to the image when an error occurs. The default value is `false`.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description for software update installation schedule.

`LastRunDateTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Last run time for software update installation.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name for software update installation schedule.

`Schedule` Data type: `String`

Access type: Read/Write

Qualifiers: none

Schedule for software update installation schedule.

`ScheduleID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

ID for software update installation schedule.

`State` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

State for software update installation at this scheduled time.

| Value | Installation state |
| --- | --- |
| 0 | None |
| 1 | Scheduled |
| 2 | Running |
| 3 | Succeeded |
| 4 | Failed |

`UpdateDP` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`True` to specify whether to update distribution points with the image after the software updates are successfully applied. The image might not be available until the image distribution is complete.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
