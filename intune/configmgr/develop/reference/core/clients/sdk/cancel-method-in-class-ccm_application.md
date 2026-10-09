---
description: Learn how to cancel an application deployment using the Cancel class method in Configuration Manager.
title: "Cancel Method in Class CCM_Application"
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

# Cancel Method in Class CCM_Application

The `Cancel` Windows Management Instrumentation (WMI) class method in Configuration Manager that cancels an application deployment.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 Cancel
{
    [IN]    String Id
    [IN]    String Revision
    [IN]    Boolean IsMachineTarget
};
```

## Parameters

`Id` Data type: `String`

Qualifiers: [id("0"), in]

Application identifier.

`Revision` Data type: `String`

Qualifiers: [id("1"), in]

Revision.

`IsMachineTarget` Data type: `Boolean`

Qualifiers: [id("2"), in]

`true` if the application targets a device.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
