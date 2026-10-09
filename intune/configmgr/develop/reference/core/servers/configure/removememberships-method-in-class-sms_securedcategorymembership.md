---
title: "RemoveMemberships Method in Class SMS_SecuredCategoryMembership"
description: The RemoveMemberships Windows Management Instrumentation (WMI) class method is a batch operation to remove objects from categories.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/86a4b315-a9f1-4577-b985-6fb0e0e67420
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/96ac410d-d052-4707-8007-df31dd0fe041
---

# RemoveMemberships Method in Class SMS_SecuredCategoryMembership

The `RemoveMemberships` Windows Management Instrumentation (WMI) class method, in Configuration Manager, is a batch operation to remove objects from categories.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RemoveMemberships(
    String   ObjectIDs[],
    Uint32   ObjectTypeIDs[],
    String   CategoryIDs[]
);
```

#### Parameters

`ObjectIDs` Data type: `String` Array

Qualifiers: [in]

The array of object IDs.

`ObjectTypeIDs` Data type: `UInt32` Array

Qualifiers: [in]

The array of corresponding object type ID.

`CategoryIDs` Data type: `String` Array

Qualifiers: [in]

The array of corresponding security category IDs which those objects will be removed from.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SecuredCategoryMembership Server WMI Class](sms_securedcategorymembership-server-wmi-class.md)
