---
title: "SMS_BoundaryGroupSiteSystems Server WMI Class"
description: The SMS_BoundaryGroupSiteSystems WMI class represents site systems that serve computers within the boundary group.
ms.date: "2017-03-13T00:00:00Z"
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

# SMS_BoundaryGroupSiteSystems Server WMI Class

The `SMS_BoundaryGroupSiteSystems` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents site systems that serve computers within the boundary group.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_BoundaryGroupSiteSystems : SMS_BaseClass
{
    UInt32 Flags;
    UInt32 GroupID;
    String ServerNALPath;
    String SiteCode;
};
```

## Methods

The `SMS_BoundaryGroupSiteSystems` class does not define any methods.

## Properties

`Flags` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [bits]

Specifies the connection type of the boundary. Possible values are:

| Value | Description |
| --- | --- |
| 0 | FAST |
| 1 | SLOW |

> [!NOTE]
>
> This parameter is no longer used for distribution points.

`GroupID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Unique identifier of the boundary group.

`ServerNALPath` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

NAL path of site system servicing machines within the boundary.

`SiteCode` Data type: `String`

Access type: Read-only

Qualifiers: [read, sizelimit("3")]

Site code of the role.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
