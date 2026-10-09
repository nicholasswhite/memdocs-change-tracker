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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1cfdec6-b0c3-4209-818c-736879856e0e
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/37da4cc9-0cfc-42a9-ba5e-805706b01ef8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/2d0723c1-cf38-4c30-ab3d-5df787b33270
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3661fb96-d414-4a4e-b7ad-9370637790dd
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
