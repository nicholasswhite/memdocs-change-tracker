---
title: "AddDistributionPoints Method in Class SMS_BootImagePackage"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn about the simplified syntax, parameters, return values, and requirements of the AddDistributionPoints method.
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

# AddDistributionPoints Method in Class SMS_BootImagePackage

The `AddDistributionPoints` Windows Management Instrumentation (WMI) class method, in Configuration Manager, adds the distribution points for the boot image package.

> [!NOTE]
>
> The `AddDistributionPoints` method allows a list of distribution points to be added to a package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 AddDistributionPoints(
      String SiteCode[],
      String NALPath[]
);
```

#### Parameters

`SiteCode` Data type: `String` Array

Qualifiers: [in]

The code for the site to which to add the distribution points.

`NALPath` Data type: `String` Array

Qualifiers: [in]

Network abstraction layer (NAL) path to the distribution points.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

It is not necessary to refresh the distribution points when using this method.

For more information about NAL paths, see [SMS_NAL_Methods Server WMI Class](../misc/sms_nal_methods-server-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BootImagePackage Server WMI Class](sms_bootimagepackage-server-wmi-class.md) [SMS_NAL_Methods Server WMI Class](../misc/sms_nal_methods-server-wmi-class.md)
