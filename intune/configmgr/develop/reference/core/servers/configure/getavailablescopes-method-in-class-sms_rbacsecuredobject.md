---
description: The GetAvailableScopes Windows Management Instrumentation class method, in Configuration Manager, returns the secured scopes, which current user has the permission to grant to other accounts.
title: "GetAvailableScopes Method in Class SMS_RbacSecuredObject"
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

# GetAvailableScopes Method in Class SMS_RbacSecuredObject

The `GetAvailableScopes` Windows Management Instrumentation (WMI) class method, in Configuration Manager, returns the secured scopes, which current user has the permission to grant to other accounts.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 GetAvailableScopes(
     String RoleIDs[],
     UInt32 ScopeTypeID,
     String ScopeIDs[],
     String ScopeNames[]
);
```

#### Parameters

`RoleIDs` Data type: `String` Array

Qualifiers: [in]

The role ID list which user uses to grant permissions to other accounts.

`ScopeTypeID` Data type: `UInt32`

Qualifiers: [in, optional]

Type of scope, could be RBA security category (29) or collection(1). The default value is 29.

| Value | Scope type |
| --- | --- |
| 1 | Collection |
| 29 | Secured scope. |

`ScopeIDs` Data type: `String` Array

Qualifiers: [out]

IDs of collections for which the user has the specified permissions.

`ScopeNames` Data type: `String` Array

Qualifiers: [out]

The name of the scopes.

## Return Values

A `UInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
