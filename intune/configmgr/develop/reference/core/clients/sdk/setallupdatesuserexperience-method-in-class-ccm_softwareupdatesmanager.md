---
title: "SetAllUpdatesUserExperience Method in Class CCM_SoftwareUpdatesManager"
description: In Configuration Manager, the SetAllUpdatesUserExperience WMI class method sets the user experience mode that determines how software updates are displayed on a target computer.
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

# SetAllUpdatesUserExperience Method in Class CCM_SoftwareUpdatesManager

The `SetAllUpdatesUserExperience` WMI class method, in Configuration Manager, sets the user experience mode that determines how software updates are displayed on a target computer.

> [!NOTE]
>
> This method can be used to hide or show all software updates in software center.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 SetAllUpdatesUserExperience(
     [IN]  UInt32 UserExperience
);
```

#### Parameters

`UserExperience` Data type: `UInt32`

Qualifiers: [in]

The user experience flag. The following table shows the possible user experience mode values.

| Value | User experience |
| --- | --- |
| 0 | DEFAULT (per policy) |
| 1 | INTERACTIVE |
| 2 | QUIET |

## Return Values

A `UInt32` data type that is 0 to indicate success or nonzero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Remarks

This method is only available for local administrators. When a software update deployment has been prepared and software updates are available for installation, this method and the `GetAllUpdatesUserExperience` method can be used to configure the user experience.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[CCM_SoftwareUpdatesManager Client WMI Class](ccm_softwareupdatesmanager-client-wmi-class.md)
