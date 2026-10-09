---
description: Article outlining the use of the GetSuppressComputerActivityInPresentationMode in Configuration Manager.
title: "GetSuppressComputerActivityInPresentationMode Method in Class CCM_ClientUXSettings"
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

# GetSuppressComputerActivityInPresentationMode Method in Class CCM_ClientUXSettings

The `GetSuppressComputerActivityInPresentationMode` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that gets the value for `SuppressComputerActivityInPresentationMode`

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetSuppressComputerActivityInPresentationMode
{
    [OUT]   Boolean SuppressComputerActivityInPresentationMode
};
```

## Parameters

`SuppressComputerActivityInPresentationMode` Data type: `Boolean`

Qualifiers: [id("0"), out]

`true` to suppress computer activity in presentation mode.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
