---
title: "GetCollectionsWithResourcePermissions Method in Class SMS_RbacSecuredObject"
description: In Configuration Manager, the GetCollectionsWithResourcePermissions WMI class method gets the list of collection identifiers for which the user has the specified permissions. The collection must contain the specified resource.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
---

# GetCollectionsWithResourcePermissions Method in Class SMS_RbacSecuredObject

The `GetCollectionsWithResourcePermissions` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the list of collection identifiers for which the user has the specified permissions. The collection must contain the specified resource.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 GetCollectionsWithResourcePermissions(
     UInt32 ResourceID,
     UInt32 Permissions,
     String CollectionIDs[]
);
```

#### Parameters

`ResourceID` Data type: `UInt32`

Qualifiers: [in]

Unique ID, supplied by Configuration Manager, for the resource.

`Permissions` Data type: `UInt32`

Qualifiers: [in]

Set of user permissions for the collections that contain the resource.

`CollectionIDs` Data type: `String` Array

Qualifiers: [out]

IDs of collections for which the user has the specified permissions.

## Return Values

A `UInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_RbacSecuredObject Server WMI Class](sms_rbacsecuredobject-server-wmi-class.md)
