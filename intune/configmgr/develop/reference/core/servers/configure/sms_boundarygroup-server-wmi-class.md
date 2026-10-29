---
title: "SMS_BoundaryGroup Server WMI Class"
description: The SMS_BoundaryGroup WMI class is an SMS Provider server class that represents a boundary group defined in the site hierarchy.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_BoundaryGroup Server WMI Class

The `SMS_BoundaryGroup` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a boundary group defined in the site hierarchy.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_BoundaryGroup : SMS_BaseClass
{
    String CreatedBy;
    DateTime CreatedOn;
    String DefaultSiteCode;
    String Description;
    UInt64 Flags;
    UInt32 GroupID;
    UInt32 MemberCount;
    String ModifiedBy;
    DateTime ModifiedOn;
    String Name;
    Boolean Shared;
    UInt32 SiteSystemCount;
};
```

## Methods

The following table lists the methods in the `SMS_BoundaryGroup` class.

| Method | Description |
| --- | --- |
| [AddBoundary Method in Class SMS_BoundaryGroup](addboundary-method-in-class-sms_boundarygroup.md) | Adds boundaries to this boundary group. |
| [AddSiteSystem Method in Class SMS_BoundaryGroup](addsitesystem-method-in-class-sms_boundarygroup.md) | Adds a site system to this boundary group. |
| [RemoveBoundary Method in Class SMS_BoundaryGroup](removeboundary-method-in-class-sms_boundarygroup.md) | Removes boundaries from this boundary group. |
| [RemoveSiteSystem Method in Class SMS_BoundaryGroup](removesitesystem-method-in-class-sms_boundarygroup.md) | Removes site systems from this boundary group. |

## Properties

`CreatedBy` Data type: `String`

Access type: Read-only

Qualifiers: [read]

User that created the boundary group.

`CreatedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date the boundary group was created.

`DefaultSiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [sizelimit("3")]

Site code new clients will be auto assigned to.

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description for the boundary group.

`Flags`  
 Data type: `UInt64`

Access type: Read/Write

Qualifiers: none

Boundary group property flags.

| Value | Execution context |
| --- | --- |
| 0 | Allow peer downloads in this boundary group |
| 1 | Allow peer downloads in this boundary group **is not enabled** |
| 2 | During peer downloads, only use peers within the same subnet |
| 4 | Prefer distribution points over peers within the same subnet |
| 8 | Prefer cloud based sources over on-premises sources |

> [!NOTE]
>
> These are binary flags. So multiple can be set at once. E.g. if a value of 6 is shown, then the first 3 are enabled.

`GroupID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Auto-generated unique identifier for the boundary group.

`MemberCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of boundaries in the boundary group.

`ModifiedBy` Data type: `String`

Access type: Read-only

Qualifiers: [read]

User that last modified the boundary group.

`ModifiedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date the boundary group was last modified.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null, unique]

Name of the boundary group.

`Shared` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

`true` if this boundary group was created by migration manager for a shared distribution point.

`SiteSystemCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Site system count.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
