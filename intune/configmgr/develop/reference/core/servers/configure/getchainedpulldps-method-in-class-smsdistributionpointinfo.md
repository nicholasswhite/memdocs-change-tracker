---
title: "GetChainedPullDPs Method in Class SMSDistributionPointInfo"
description: The GetChainedPullDPs WMI class method, in Configuration Manager, ensures that when a source distribution point is assigned, a looping chain isn't generated.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/0850fefd-e402-4507-ae98-46cfdfc2e16c
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6ecf98a5-97c7-4249-b209-a9d9e42633a0
---

# GetChainedPullDPs Method in Class SMSDistributionPointInfo

The `GetChainedPullDPs` Windows Management Instrumentation (WMI) class method, in Configuration Manager, ensures that when a source distribution point is assigned, a looping chain isn't generated. (If distribution point 1 is the source of distribution point 2, and distribution point 2 is the source of distribution point 3, then distribution point 3 can't be source of distribution point 1).

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 GetChainedPullDPs(
     string SourceDPNALPath,
     string ChainedDPs[]
);
```

#### Parameters

`SourceDPNALPath` Data type: `String`

Qualifiers: `[in]`

Source distribution point NAL path.

`ChainedDPs` Data type: `String` Array

Qualifiers: `[out]`

An array of chained distribution points.

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
