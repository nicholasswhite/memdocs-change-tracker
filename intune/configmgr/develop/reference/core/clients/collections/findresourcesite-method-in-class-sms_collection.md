---
title: "FindResourceSite Method in Class SMS_Collection"
description: In Configuration Manager, the FindResourceSite WMI class method gets site code information for resources.
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

# FindResourceSite Method in Class SMS_Collection

The `FindResourceSite` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets site code information for resources.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 FindResourceSite(
        boolean IncludeSubCollections = false,
        string SiteCode[],
        uint32 ResourceNumber[]
);

```

#### Parameters

`IncludeSubCollections` Data type: `Boolean`

Qualifiers: [in, optional, deprecated]

true if subcollections are also marked for evaluation. If this parameter is set to false, subcollections are not included. The value defaults to false, if not specified.

`SiteCode[]` Data type: `String` Array

Qualifiers: [out]

Site code of the site with which the resource is associated.

`ResourceNumber` Data type: `UInt32` Array

Qualifiers: [out]

Configuration Manager supplied ID that uniquely identifies a client resource.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) [SMS_Site Server WMI Class](../../servers/configure/sms_site-server-wmi-class.md)
