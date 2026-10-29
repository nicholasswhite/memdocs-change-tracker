---
description: Learn how to represent a default boundary group using SMS_DefaultBoundaryGroup Windows Management Instrumentation (WMI) class.
title: "SMS_DefaultBoundaryGroup Server WMI Class"
ms.date: "2017-03-13T00:00:00Z"
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

# SMS_DefaultBoundaryGroup Server WMI Class

The `SMS_DefaultBoundaryGroup` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a default boundary group.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DefaultBoundaryGroup : SMS_BaseClass
{
    String CreatedBy;
    DateTime CreatedOn;
    String DefaultSiteCode;
    String Description;
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

The following table shows the methods in `SMS_DefaultBoundaryGroup`.

| Method | Description |
| --- | --- |
| [AddBoundary Method in Class SMS_DefaultBoundaryGroup](addboundary-method-in-class-sms-defaultboundarygroup.md) | Adds one or more boundaries to a default boundary group. |
| [AddSiteSystem Method in Class SMS_DefaultBoundaryGroup](addsitesystem-method-in-class-sms-defaultboundarygroup.md) | Adds one or more site system servers to a default boundary group. |
| [RemoveBoundary Method in Class SMS_DefaultBoundaryGroup](removeboundary-method-in-class-sms-defaultboundarygroup.md) | Removes one or more boundaries from a default boundary group. |
| [RemoveSiteSystem Method in Class SMS_DefaultBoundaryGroup](removesitesystem-method-in-class-sms-defaultboundarygroup.md) | Removes one or more site system servers from a default boundary group. |

## Properties

`CreatedBy` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Name of the user who created the default boundary group.

`CreatedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date and time that the default boundary group was created.

`DefaultSiteCode` Data type: `String`

Access type: Read-only

Qualifiers: [read, SizeLimit("3")]

The site code to which new clients will be automatically assigned.

`Description` Data type: `String`

Access type: Read-only

Qualifiers: [read]

A description for the boundary group.

`GroupID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

An automatically-generated unique ID for the boundary group.

`MemberCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of members in the boundary group. The default value is 0.

`ModifiedBy` Data type: `String`

Access type: Read-only

Qualifiers: [read]

User who modified the boundary group.

`ModifiedOn` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

Date and time that the boundary group was modified.

`Name` Data type: `String`

Access type: Read-only

Qualifiers: [read, unique, not_null]

Name of the boundary group.

`Shared` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

Indicates whether the boundary group was created by Migration Manager for a shared distribution point.

`SiteSystemCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Count of site system servers that are associated with the boundary group. The default value is 0.

## Remarks

Class qualifiers for this class include:

- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BoundaryGroup Server WMI Class](sms_boundarygroup-server-wmi-class.md)

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
