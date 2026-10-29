---
description: Learn how to use the GetFileBinary Method to get the binary user interface for a feature.
title: "GetFileBinary Method in Class SMS_Identification"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# GetFileBinary Method in Class SMS_Identification

The `GetFileBinary` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the binary user interface for a feature. The binary can be separated into multiple blocks starting with number 1. If `isTheLastBlock` equals `False`, then you need call the method again with blockNumber+1 to get the next block.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetFileBinary (
    String FileName,
    UInt32 blockNumber,
    String binary64Encoded,
    Boolean isTheLastBlock
);

```

#### Parameters

`FileName` Data type: `String`

Qualifiers: [in]

The name of the file.

`blockNumber` Data type: `UInt32`

Qualifiers: [in]

The block number. To get the next block, call the method again with blockNumber+1, as long as isTheLastBlock equals `False`.

`binary64Encoded` Data type: `String`

Qualifiers: [out]

The binary 64-encoded file.

`isTheLastBlock` Data type: `Boolean`

Qualifiers: [out]

`True` if the current block is the last block; otherwise, `False`. While `False`, you can get the next block by calling the method again with blockNumber+1.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Identification Server WMI Class](sms_identification-server-wmi-class.md)
