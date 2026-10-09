---
title: "ImportRole Method in Class SMS_Role"
description: The ImportRole Windows Management Instrumentation (WMI) class method imports a role defined by an XML string to the database.
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

# ImportRole Method in Class SMS_Role

The `ImportRole` Windows Management Instrumentation (WMI) class method, in Configuration Manager, imports a role defined by an XML string to the database.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ImportRole(
     String RolesXml,
     Boolean OverwrittenExisted,
     String ErrorStr,
);
```

#### Parameters

`RolesXml` Data type: `String`

Qualifiers: [in]

The id of the role.

`OverwrittenExisted` Data type: `Boolean`

Qualifiers: [in]

`true`, if an existing role should be overwritten. The default value is true.

`ErrorStr` Data type: `String`

Qualifiers: [out]

The error information if there is any error while importing the role.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Role Server WMI Class](sms_role-server-wmi-class.md)
