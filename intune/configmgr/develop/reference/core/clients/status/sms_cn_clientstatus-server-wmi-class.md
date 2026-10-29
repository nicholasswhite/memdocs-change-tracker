---
title: "SMS_CN_ClientStatus Server WMI Class"
description: The SMS_CN_ClientStatus Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that represents client notification of agent status.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CN_ClientStatus Server WMI Class

The `SMS_CN_ClientStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents client notification of agent status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CN_ClientStatus : SMS_BaseClass
{
    UInt32 ChannelType;
    DateTime LastStatusTime;
    UInt32 OnlineStatus;
    UInt32 ResourceID;
    UInt32 ServerID;
};
```

## Methods

The following table lists the methods in the `SMS_CN_ClientStatus` class.

| Method | Description |
| --- | --- |
| [GetOnlineCount Method in Class SMS_CN_ClientStatus](getonlinecount-method-in-class-sms_cn_clientstatus.md) | Gets an online count of the selected clients of the target collection. |

## Properties

`ChannelType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Channel type. Possible values are:

| Value | Channel type |
| --- | --- |
| 0 | TCP |
| 1 | HTTP |

`LastStatusTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Last online time.

`OnlineStatus` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Online status. Possible values are:

| Value | Online status |
| --- | --- |
| 0 | Offline |
| 1 | Online |

`ResourceID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Client resource identifier.

`ServerID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Client notification server identifier.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
