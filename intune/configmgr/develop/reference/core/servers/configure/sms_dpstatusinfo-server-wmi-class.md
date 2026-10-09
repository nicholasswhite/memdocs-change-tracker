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
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
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
