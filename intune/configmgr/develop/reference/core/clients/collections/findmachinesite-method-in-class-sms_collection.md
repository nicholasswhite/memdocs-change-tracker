---
title: "FindMachineSite Method in Class SMS_Collection"
description: In Configuration Manager, the FindMachineSite Windows Management Instrumentation class method gets site code information for a specific resource.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# FindMachineSite Method in Class SMS_Collection

The `FindMachineSite` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets site code information for a specific resource.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 FindMachineSite(
        uint32 ResourceID,
        string SiteCode[]
);

```

#### Parameters

`ResourceID` Data type: `UInt32`

Qualifiers: [in]

Configuration Manager supplied ID that uniquely identifies a client resource.

`SiteCode[]` Data type: `String` Array

Qualifiers: [out]

Site code of the site with which the resource is associated.

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
