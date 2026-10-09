---
title: "AddSiteSystem Method in Class SMS_BoundaryGroup"
description: Learn how to add a site system to a boundary group in Configuration Manager using the AddSiteSystem class.
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

# AddSiteSystem Method in Class SMS_BoundaryGroup

The `AddSiteSystem` Windows Management Instrumentation (WMI) class method, in Configuration Manager, adds a site system to this boundary group.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 AddSiteSystem(
   String ServerNALPath[];
   UInt32 Flags[]
);
```

#### Parameters

`ServerNALPath` Data type: `String` Array

Qualifiers: [in]

Network abstraction layer (NAL) path to the site system.

`Flags` Data type: `UInt32` Array

Qualifiers: [in]

Identifies the network connection speed between the site system server and the connecting clients. Possible values are:

| Value | Connection speed |
| --- | --- |
| 0 | Fast |
| 1 | Slow |

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BoundaryGroup Server WMI Class](sms_boundarygroup-server-wmi-class.md)
