---
description: The SMS_DistributionStatus WMI class is an SMS Provider server class, in Configuration Manager, that represents the status of a package that has been assigned to a distribution point.
title: "SMS_DistributionStatus Server WMI Class"
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

# SMS_DistributionStatus Server WMI Class

The `SMS_DistributionStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that represents the status of a package that has been assigned to a distribution point.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DistributionStatus : SMS_BaseClass
{
    UInt32 Assets;
    DateTime LastUpdateDate;
    UInt32 MessageCategory;
    String ObjectID;
    UInt32 ObjectTypeID;
    String PackageID;
    UInt32 Type;
};
```

## Methods

The `SMS_DistributionStatus` class doesn't define any methods.

## Properties

`Assets` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Number of distribution points in this status.

`LastUpdateDate` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Last status update date.

`MessageCategory` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Status message category.

`ObjectID` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

PackageID or ModelName.

`ObjectTypeID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Secured object class ID.

| Value | Object type |
| --- | --- |
| 2 | SMS_DistributionStatus |
| 14 | SMS_OperatingSystemInstallPackage |
| 18 | SMS_ImagePackage |
| 19 | SMS_BootImagePackage |
| 21 | SMS_DeviceSettingPackage |
| 23 | SMS_DriverPackage |
| 24 | SMS_SoftwareUpdatesPackage |
| 31 | SMS_Application |

`PackageID` Data type: `String`

Access type: Read-only

Qualifiers: [read]

PackageID.

`Type` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Status Type.

| Value | Status type |
| --- | --- |
| 1 | Success |
| 2 | InProgress |
| 3 | Error |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
