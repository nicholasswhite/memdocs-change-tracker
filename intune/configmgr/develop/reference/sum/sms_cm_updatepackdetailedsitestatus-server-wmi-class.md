---
title: "SMS_CM_UpdatePackDetailedSiteStatus Server WMI Class"
description: "In Configuration Manager, the  SMS_CM_UpdatePackDetailedSiteStatus WMI class is an SMS Provider server class that is used to get detailed update package installation status per site."
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

# SMS_CM_UpdatePackDetailedSiteStatus Server WMI Class

The `SMS_CM_UpdatePackDetailedSiteStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that is used to get detailed update package installation status per site.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CM_UpdatePackDetailedSiteStatus : SMS_BaseClass  
{  
    DateTime MessageTime;  
    String PackageGuid;  
    String SiteCode;  
    SInt32 SiteInstallID;  
    SInt32 SiteNumber;  
    String StatusDescription;  
    SInt32 StatusID;  
    String StatusName;  
    SInt32 SubStatusID;  
};  

```

## Methods

The `SMS_CM_UpdatePackDetailedSiteStatus` class does not define any methods.

## Properties

`MessageTime`  
 Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The time that the message was created.

`PackageGuid`  
 Data type: `String`

Access type: Read-only

Qualifiers: [read]

Unique identifier of the update package.

`SiteCode`  
 Data type: `String`

Access type: Read-only

Qualifiers: [read, key, not_null]

Unique identifier of the site.

`SiteInstallID`  
 Data type: `SInt32`

Access type: Read-only

Qualifiers: [read, key, not_null]

The number of installation retires.

`SiteNumber`  
 Data type: `Sint32`

Access type: Read-only

Qualifiers: [read, key, not_null]

Unique identifier of the site.

`StatusDescription`  
 Data type: `String`

Access type: Read-only

Qualifiers: [read]

Description of the status.

`StatusID`  
 Data type: `Sint32`

Access type: Read-only

Qualifiers: [read, key, not_null]

The status ID.

`StatusName`  
 Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the status.

`SubStatusID`  
 Data type: `SInt32`

Access type: Read-only

Qualifiers: [read, key, not_null]

The ID of the `SubStatus`.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
