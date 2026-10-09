---
title: "SMS_MDMBulkEnrollmentPackages Server WMI Class"
description: The SMS_MDMBulkEnrollmentPackages WMI class is an SMS Provider server class that represents on-premises Mobile Device Management bulk enrollment packages.
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

# SMS_MDMBulkEnrollmentPackages Server WMI Class

The `SMS_MDMBulkEnrollmentPackages` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents On-premises Mobile Device Management (MDM) bulk enrollment packages.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MDMBulkEnrollmentPackages : SMS_BaseClass
{
    String CertificateId;
    DateTime CreationTime;
    DateTime ExpiryTime;
    UInt32 Package_ID;
    String PackageName;
    UInt32 Profile_ID;
    String  Profile_UniqueID;
    String ProfileName;
    UInt32 State;
};

```

## Methods

The following table lists the methods in the `SMS_MDMBulkEnrollmentPackages` class.

| Method | Description |
| --- | --- |
| [ImportForProfile Method in Class SMS_MDMBulkEnrollmentPackages](importforprofile-method-in-class-sms_mdmbulkenrollmentpackages.md) | Imports an MDM bulk enrollment package for a profile. |

## Properties

`CertificateId` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique certificate ID, as a GUID.

`CreationTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The time the package was created.

`ExpiryTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The time the package expires.

`Package_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Package ID.

`PackageName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Package name.

`Profile_ID` Data type: `uint32`

Access type: Read/Write

Qualifiers: [key]

Profile ID.

`Profile_UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: [unique, not_null]

Unique ID of the Profile.

`ProfileName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Profile name.

`State` Data type: `uint32`

Access type: Read/Write

Qualifiers: none

State of the package.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
