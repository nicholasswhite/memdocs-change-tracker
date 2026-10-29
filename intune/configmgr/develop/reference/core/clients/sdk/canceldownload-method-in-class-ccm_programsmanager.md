---
description: Learn how the CancelDownload WMI class method, in Configuration Manager, cancels jobs that are downloading content that is required for legacy software distribution programs.
title: "CancelDownload Method in Class CCM_ProgramsManager"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CancelDownload Method in Class CCM_ProgramsManager

The `CancelDownload` WMI class method, in Configuration Manager, cancels jobs that are downloading content that is required for legacy software distribution programs.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 CancelDownload(
     [IN]  String ProgramID,
     [IN]  String PackageID
);
```

#### Parameters

`ProgramID` Data type: `String`

Qualifiers: [in]

Identifier of the software distribution program.

`PackageID` Data type: `String`

Qualifiers: [in]

Identifier of the associated software distribution package.

## Return Values

A `UInt32` data type that is 0 to indicate success or nonzero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[CCM_ProgramsManager Client WMI Class](ccm_programsmanager-client-wmi-class.md)
