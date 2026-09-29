---
description: Learn how to remove one or more site system servers from a default boundary group using the RemoveSiteSystem class.
title: "RemoveSiteSystem Method in Class SMS_DefaultBoundaryGroup"
ms.date: "2017-03-13T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# RemoveSiteSystem Method in Class SMS_DefaultBoundaryGroup

The `RemoveSiteSystem` Windows Management Instrumentation (WMI) class method, in Configuration Manager, removes one or more site system servers from a default boundary group.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 RemoveSiteSystem(
    String ServerNALPath[]
);
```

### Parameters

`ServerNALPath` Data type: `String`

Qualifiers: [in]

Array of network abstraction layer (NAL) paths to one or more site system servers within the boundary group.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_DefaultBoundaryGroup Server WMI Class](sms-defaultboundarygroup-server-wmi-class.md)
