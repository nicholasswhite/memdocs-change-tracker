---
description: Learn how to map a role and its associated object types in Configuration Manager using the SMS_RoleInObjectType class.
title: "SMS_RoleInObjectType Server WMI Class"
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

# SMS_RoleInObjectType Server WMI Class

The `SMS_RoleInObjectType` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that maps a role and its associated object types.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_RoleInObjectType : SMS_BaseClass
{
    UInt32 ObjectTypeID;
    String RoleID;
};
```

## Methods

The `SMS_RoleInObjectType` class doesn't define any methods.

## Properties

`ObjectTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Secured object class ID. Possible values are listed below.

| Value | Object type ID |
| --- | --- |
| 2 | SMS_Package |
| 14 | SMS_OperatingSystemInstallPackage |
| 18 | SMS_ImagePackage |
| 19 | SMS_BootImagePackage |
| 21 | SMS_DeviceSettingPackage |
| 23 | SMS_DriverPackage |
| 24 | SMS_SoftwareUpdatesPackage |
| 31 | SMS_Application |

`RoleID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The ID of the role.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
