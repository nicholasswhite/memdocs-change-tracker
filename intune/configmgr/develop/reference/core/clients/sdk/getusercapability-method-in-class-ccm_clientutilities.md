---
title: "GetUserCapability Method in Class CCM_ClientUtilities"
description: The GetUserCapability WMI class method in Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetUserCapability Method in Class CCM_ClientUtilities

The `GetUserCapability` Windows Management Instrumentation (WMI) class method in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetUserCapability
{
    [IN]    UInt32 Feature
    [OUT]   UInt32 Value
};
```

## Parameters

`Feature` Data type: `UInt32`

Qualifiers: [id("0"), in]

Feature.

`Value` Data type: `UInt32`

Qualifiers: [id("1"), out]

Value.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
