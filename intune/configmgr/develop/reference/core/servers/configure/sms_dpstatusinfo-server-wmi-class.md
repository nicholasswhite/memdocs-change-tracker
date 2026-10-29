---
title: "SMS_DPStatusInfo Server WMI Class"
description: Learn how the SMS_DPStatusInfo class is an SMS Provider server class, in Configuration Manager, that represents distribution point status information.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_DPStatusInfo Server WMI Class

The `SMS_DPStatusInfo` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents distribution point status information.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DPStatusInfo : SMS_BaseClass
{
    Boolean IsDPMonEnabled;
    Boolean IsMulticast;
    Boolean IsPullDP;
    Boolean IsPXE;
    DateTime LastStatusTime;
    UInt32 MessageCount;
    UInt32 MessageState;
    String NALPath;
    String Name;
    UInt32 NumberErrors;
    UInt32 NumberInProgress;
    UInt32 NumberInstalled;
    UInt32 NumberUnknown;
    String Version;
};
```

## Methods

The `SMS_DPStatusInfo` class does not define any methods.

## Properties

`IsDPMonEnabled` Data type: `Boolean`

Access type: Read-only

Qualifiers: [not_null, read]

`true` if this distribution point is monitored by distribution point monitor.

`IsMulticast` Data type: `Boolean`

Access type: Read-only

Qualifiers: [not_null, read]

`true` if this distribution point is multicast enabled.

`IsPullDP` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read, not_null]

`true` if this is a pull distribution point.

`IsPXE` Data type: `Boolean`

Access type: Read-only

Qualifiers: [not_null, read]

`true` if this distribution point is PXE enabled.

`LastStatusTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Time of the last status message.

`MessageCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Count of the number of messages on this distribution point.

`MessageState` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

State of the message.

| Value | Message state |
| --- | --- |
| 1 | Success |
| 2 | InProgress |
| 3 | Error |

`NALPath` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

Distribution point NAL path.

`Name` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the distribution point.

`NumberErrors` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Count of the failed content installations.

`NumberInProgress` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Count of the content installations in progress.

`NumberInstalled` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Count of the installed content.

`NumberUnknown` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Count of the unknown content.

`Version` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Version to which the distribution point is upgraded.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
