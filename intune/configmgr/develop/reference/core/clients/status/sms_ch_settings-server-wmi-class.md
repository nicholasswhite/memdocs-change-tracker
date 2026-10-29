---
title: "SMS_CH_Settings Server WMI Class"
description: Learn how the SMS_CH_Settings class is an SMS Provider server class, in Configuration Manager, that represents client status settings.
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

# SMS_CH_Settings Server WMI Class

The `SMS_CH_Settings` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents client status settings.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CH_Settings : SMS_BaseClass
{
    String ADRetrievingSchedule;
    UInt32 CleanUpInterval;
    UInt32 DDRInactiveInterval;
    UInt32 HWInactiveInterval;
    Boolean NeedADLastLogonTime;
    UInt32 PolicyInactiveInterval;
    UInt32 SettingsID;
    UInt32 StatusInactiveInterval;
    UInt32 SWInactiveInterval;
};
```

## Methods

The `SMS_CH_Settings` class does not define any methods.

## Properties

`ADRetrievingSchedule` Data type: `String`

Access type: Read/Write

Qualifiers: none

Schedule for how frequently the system retrieves information from Active Directory.

`CleanUpInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

History clean up interval.

`DDRInactiveInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Heartbeat discovery inactive interval.

`HWInactiveInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Hardware inventory inactive interval.

`NeedADLastLogonTime` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Last logged on time from Active Directory.

`PolicyInactiveInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Policy request inactive interval.

`SettingsID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Settings ID.

`StatusInactiveInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Status message inactive interval.

`SWInactiveInterval` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Software inventory inactive interval.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
