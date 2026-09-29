---
title: "SMS_ImageUpdateHistory Server WMI Class"
description: The SMS_ImageUpdateHistory Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents software update installation history of offline servicing image.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SMS_ImageUpdateHistory Server WMI Class

The `SMS_ImageUpdateHistory` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents software update installation history of offline servicing image.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ImageUpdateHistory : SMS_BaseClass
{
    SInt32 FailedUpdateID;
    String ImagePackageID;
    DateTime RunDateTime;
    SInt32 ScheduleID;
    SInt32 Status;
};
```

## Methods

The `SMS_ImageUpdateHistory` class does not define any methods.

## Properties

`FailedUpdateID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

ID for software update that failed to install.

`ImagePackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID for offline servicing image.

`RunDateTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: [key]

Last run time for software update.

`ScheduleID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

ID for software update installation schedule.

`Status` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

Software update installation status.

| Value | Installation status |
| --- | --- |
| 2 | Success |
| 3 | Failed |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
