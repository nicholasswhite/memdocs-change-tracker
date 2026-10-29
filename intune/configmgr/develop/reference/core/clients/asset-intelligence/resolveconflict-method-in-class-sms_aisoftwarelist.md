---
title: "ResolveConflict Method in Class SMS_AISoftwareList"
description: In Configuration Manager, the ResolveConflict Windows Management Instrumentation class method is used to resolve conflicts that result by creating or editing software entries, and the same software entry created by Microsoft through the online synchronization.
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

# ResolveConflict Method in Class SMS_AISoftwareList

The `ResolveConflict` Windows Management Instrumentation (WMI) class method, in Configuration Manager, is used to resolve conflicts that result by creating or editing software entries, and the same software entry being created by Microsoft through the online synchronization.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ResolveConflict(
     String SoftwareKey,
     UInt32 Resolution
);
```

#### Parameters

`SoftwareKey` Data type: `String`

Qualifiers: [in]

The MD5 hash of the software entry, which has a conflict to be resolved. The hash is made up of the software name, publisher, and version.

This property name has changed from `SoftwarePropertiesHash` to `SoftwareKey` in SP1.

`Resolution` Data type: `UInt32`

Qualifiers: [in]

Action to take on the software entry.

| Value | Description |
| --- | --- |
| 1 | Keep the local copy and discard any updates from Microsoft. |
| 2 | Revert the local copy and replace it with latest update from Microsoft. |

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_AISoftwareList Server WMI Class](sms_aisoftwarelist-server-wmi-class.md)
