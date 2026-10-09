---
title: "AddDistributionPoints Method in Class SMS_DistributionPointGroup"
description: AddDistributionPoints Windows Management Instrumentation (WMI) class method adds distribution points to the distribution point group.
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

# AddDistributionPoints Method in Class SMS_DistributionPointGroup

The `AddDistributionPoints` Windows Management Instrumentation (WMI) class method, in Configuration Manager, adds distribution points to the distribution point group.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 AddDistributionPoints(
     string DPNALPath[],
     boolean AddTargetedPackages
);
```

#### Parameters

`DPNALPath` Data type: `String` Array

Qualifiers: `[in]`

Distribution point NAL path.

`AddTargetedPackages` Data type: `Boolean`

Qualifiers: `[in, optional]`

`True` if

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Application Server WMI Class](../../../apps/sms_application-server-wmi-class.md)
