---
description: Learn how to use the Stop method to stop a Microsoft Azure service that represents a cloud distribution point for Configuration Manager.
title: "Stop method in class SMS_AzureService"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Stop method in class SMS_AzureService

The `Stop` WMI class method in Configuration Manager that's invoked to stop a Microsoft Azure service that represents a cloud distribution point for Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 Stop
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
