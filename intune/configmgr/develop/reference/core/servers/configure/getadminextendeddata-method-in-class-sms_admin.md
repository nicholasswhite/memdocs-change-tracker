---
description: Learn how to get the extended data that the current user and its groups have using GetAdminExtendedData.
title: "GetAdminExtendedData Method in Class SMS_Admin"
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

# GetAdminExtendedData Method in Class SMS_Admin

The `GetAdminExtendedData` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the extended data that the current user and its groups have for a given type.

> [!WARNING]
>
> This method is reserved for internal use.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 GetAdminExtendedData(
    [in] uint32 Type,
    [out] string ExtendedData[]);
};
```

#### Parameters

`Type` Data type: `UInt32`

Qualifiers: [in]

The type associated with the user.

`ExtendedData` Data type: `String` Array

Qualifiers: [out]

The extended data that the current user and its groups have for a given type.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Admin Server WMI Class](sms_admin-server-wmi-class.md)
