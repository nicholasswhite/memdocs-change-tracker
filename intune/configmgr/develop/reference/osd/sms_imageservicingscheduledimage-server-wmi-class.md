---
title: "SMS_ImageServicingScheduledImage Server WMI Class"
description: The SMS_ImageServicingScheduledImage WMI class represents all schedules for offline servicing image.
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

# SMS_ImageServicingScheduledImage Server WMI Class

The `SMS_ImageServicingScheduledImage` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents all schedules for offline servicing image.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ImageServicingScheduledImage : SMS_BaseClass
{
    String ImagePackageID;
    SInt32 ScheduleID;
};
```

## Methods

The `SMS_ImageServicingScheduledImage` class does not define any methods.

## Properties

`ImagePackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID for offline servicing image that is installed on client computer.

`ScheduleID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

ID for offline servicing image installation schedule.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
