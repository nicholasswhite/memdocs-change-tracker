---
title: "Start method in class SMS_AzureService"
description: In Configuration Manager, The Start WMI class method is invoked to start a Microsoft Azure service that represents a cloud distribution point for Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68ec7f3a-2bc6-459f-b959-19beb729907d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/90370425-aca4-4a39-9533-d52e5e002a5d
---

# Start method in class SMS_AzureService

The `Start` WMI class method in Configuration Manager that's invoked to start a Microsoft Azure service that represents a cloud distribution point for Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 Start
{
    [IN]    UInt32 AzureServiceID
};
```

## Parameters

`AzureServiceID` Data type: `UInt32`

Qualifiers: [id("0"), in]

The service identifier key for the `SMS_AzureService` instance on which the current task will be performed.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
