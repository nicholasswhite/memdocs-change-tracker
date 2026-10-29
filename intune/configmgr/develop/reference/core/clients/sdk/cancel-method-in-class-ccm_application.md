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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
