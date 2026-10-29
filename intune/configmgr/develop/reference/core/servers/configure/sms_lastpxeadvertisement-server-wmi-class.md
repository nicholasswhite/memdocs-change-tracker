---
description: Learn how to represent the last PXE advertisement using the SMS_LastPXEAdvertisement class in Configuration Manager.
title: "SMS_LastPXEAdvertisement Server WMI Class"
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

# SMS_LastPXEAdvertisement Server WMI Class

The `SMS_LastPXEAdvertisement` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the last PXE advertisement.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_LastPXEAdvertisement : SMS_BaseClass
{
    String AdvertisementID;
    DateTime LastPXEAdvertisementTime;
    String NetbiosName;
    UInt32 ResourceId;
    String SMBIOSGUID;
};
```

## Methods

The `SMS_LastPXEAdvertisement` class does not define any methods.

## Properties

`AdvertisementID` Data type: `String`

Access type: Read/Write

Qualifiers: none

The advertisement ID.

`LastPXEAdvertisementTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

The time of last PXE advertisement for this equipment.

`NetbiosName` Data type: `String`

Access type: Read/Write

Qualifiers: none

The NETBIOS name for the resource, which is often the same as the host name.

`ResourceId` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Key of the item.

`SMBIOSGUID` Data type: `String`

Access type: Read/Write

Qualifiers: none

The GUID of the BIOS.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
