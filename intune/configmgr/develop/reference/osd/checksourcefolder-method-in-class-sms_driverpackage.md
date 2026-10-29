---
description: Learn how to check the state of an empty driver source folder with CheckSourceFolder class im Configuration Manager.
title: "CheckSourceFolder Method in Class SMS_DriverPackage"
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

# CheckSourceFolder Method in Class SMS_DriverPackage

The `CheckSourceFolder` Windows Management Instrumentation (WMI) class method in Configuration Manager that checks the state of an empty driver source folder.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 CheckSourceFolder
{
    [IN]    String SourceFolder
    [OUT]   SInt32 Result
};
```

## Parameters

`SourceFolder` Data type: `String`

Qualifiers: [id("0"), in]

Source folder.

`Result` Data type: `SInt32`

Qualifiers: [id("1"), out]

Results of check. Possible values are:

| Value | Result |
| --- | --- |
| 0 | No error. |
| 1 | The folder isn't in UNC format. |
| 2 | Can't read/write to the folder. |
| 4 | The folder isn't empty. |
| 8 | The folder is already used by another driver package. |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
