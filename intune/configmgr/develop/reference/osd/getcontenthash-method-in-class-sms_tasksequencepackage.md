---
title: "GetContentHash Method in Class SMS_TaskSequencePackage"
description: gets the hash of specific Configuration Manager content
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# GetContentHash Method in Class SMS_TaskSequencePackage

The `GetContentHash` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the hash of specific Configuration Manager content.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetContentHash(
      UInt32 ContentID,
      UInt32 HashAlgID,
      String Hash
);
```

#### Parameters

`ContentID` Data type: `UInt32`

Qualifiers: [in]

ID of the content.

`HashAlgID` Data type: `UInt32`

Qualifiers: [in]

The ID of the cryptographic algorithm used to hash the content.

`Hash` Data type: `String`

Qualifiers: [out]

The hash for the content.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_TaskSequencePackage Server WMI Class](sms_tasksequencepackage-server-wmi-class.md)
