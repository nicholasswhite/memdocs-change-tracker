---
title: "GetPendingComponentList Method in Class CCM_Application"
description: In Configuration Manager, the GetPendingComponentList Windows Management Instrumentation class method that gets the pending component list for an application.
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

# GetPendingComponentList Method in Class CCM_Application

The `GetPendingComponentList` Windows Management Instrumentation (WMI) class method in Configuration Manager that gets the pending component list for an application.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetPendingComponentList
{
    [IN]    String AppDeliveryTypeId
    [IN]    UInt32 Revision
    [OUT]   String PendingComponentList
};
```

## Parameters

`AppDeliveryTypeId` Data type: `String`

Qualifiers: [id("0"), in]

Application delivery type identifier.

`Revision` Data type: `UInt32`

Qualifiers: [id("1"), in]

Revision.

`PendingComponentList` Data type: `String`

Qualifiers: [id("2"), out]

Pending component list.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
