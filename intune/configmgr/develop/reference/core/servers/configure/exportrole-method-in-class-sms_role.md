---
title: "ExportRole Method in Class SMS_Role"
description: The ExportRole Windows Management Instrumentation class method, in Configuration Manager, exports roles to an XML string.
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

# ExportRole Method in Class SMS_Role

The `ExportRole` Windows Management Instrumentation (WMI) class method, in Configuration Manager, exports roles to an XML string.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ExportRole(
     String RoleID,
     String ExportedXML,
);
```

#### Parameters

`RoleID` Data type: `String`

Qualifiers: [in]

The id of the role.

`ExportedXML` Data type: `String`

Qualifiers: [out]

The XML blob for the role.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Role Server WMI Class](sms_role-server-wmi-class.md)
