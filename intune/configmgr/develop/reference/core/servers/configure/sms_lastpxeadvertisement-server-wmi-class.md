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
