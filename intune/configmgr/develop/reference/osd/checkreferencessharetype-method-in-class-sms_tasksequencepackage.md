---
title: "CheckReferencesShareType Method in Class SMS_TaskSequencePackage"
description: In Configuration Manager, the CheckReferencesShareType WMI class method checks all referred packages for this task sequence and returns all packages that aren't shared.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CheckReferencesShareType Method in Class SMS_TaskSequencePackage

The `CheckReferencesShareType` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that checks all referred packages for this task sequence and returns all packages that aren't shared.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 CheckReferencesShareType
{
    [IN]    String PackageID
    [OUT]   Boolean CanRunFromDP
    [OUT]   String PacakgeIds[]
    [OUT]   String PackageNames[]
};
```

## Parameters

`PackageID` Data type: `String`

Qualifiers: [id("0"), in]

Task sequence package identifier.

`CanRunFromDP` Data type: `Boolean`

Qualifiers: [id("1"), out]

`true` if the package can be run from the distribution point.

`PacakgeIds` Data type: `String Array`

Qualifiers: [id("2"), out]

Package identifiers for all referred packages for this task sequence that aren't shared.

> [!NOTE]
>
> The incorrect spelling of the variable "PacakgeIds" is hardcoded in WMI.

`PackageNames` Data type: `String Array`

Qualifiers: [id("3"), out]

Package names for all referred packages for this task sequence that aren't shared.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
