---
description: Learn how to represent a schedule token for events that occur for a specific time interval using SMS_ST_RecurMonthlyByWeekday class.
title: "SMS_ST_RecurMonthlyByWeekday Server WMI Class"
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

# SMS_ST_RecurMonthlyByWeekday Server WMI Class

The `SMS_ST_RecurMonthlyByWeekday` WMI class is an SMS Provider server class, in Configuration Manager, that represents a schedule token for events that occur for a specific day of the week, on a given week of the month, at a given monthly interval, for example, the second Saturday of every month.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ST_RecurMonthlyByWeekday : SMS_ScheduleToken
{
      UInt32 Day;
      UInt32 DayDuration;
      UInt32 ForNumberOfMonths;
      UInt32 HourDuration;
      Boolean IsGMT;
      UInt32 MinuteDuration;
      DateTime StartTime;
      UInt32 WeekOrder;
};
```

## Methods

The `SMS_ST_RecurMonthlyByWeekday` class does not define any methods.

## Properties

`Day` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Day of the week when the event is scheduled to occur. Possible values are listed below. The default value is 1.

| Value | Day |
| --- | --- |
| 1 | SUNDAY |
| 2 | MONDAY |
| 3 | TUESDAY |
| 4 | WEDNESDAY |
| 5 | THURSDAY |
| 6 | FRIDAY |
| 7 | SATURDAY |

`DayDuration` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Range("0-31")]

See [SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md).

`ForNumberOfMonths` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Range("1-12")]

Number of months for recurrence. Allowable values are in the range 1-12. The default value is 1.

`HourDuration` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Range("0-23")]

See [SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md).

`IsGMT` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md).

`MinuteDuration` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [Range("0-59")]

See [SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md).

`StartTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

See [SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md).

`WeekOrder` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Week of the month when the event is scheduled to occur. Possible values are listed below. The default value is 0.

| Value | Week |
| --- | --- |
| 0 | LAST |
| 1 | FIRST |
| 2 | SECOND |
| 3 | THIRD |
| 4 | FOURTH |

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ScheduleToken Server WMI Class](sms_scheduletoken-server-wmi-class.md)
