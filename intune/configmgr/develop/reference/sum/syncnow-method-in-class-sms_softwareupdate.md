---
description: Learn how to perform a manual synchronization of the Software Update Point using SyncNow class method.
title: "SyncNow Method in Class SMS_SoftwareUpdate"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3


ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SyncNow Method in Class SMS_SoftwareUpdate

The `SyncNow` Windows Management Instrumentation (WMI) class method, in Configuration Manager, performs a manual synchronization of the Software Update Point.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 SyncNow(  
     Boolean fullSync  
);  
```

#### Parameters

`fullSync`  
 Data type: `Boolean`

Qualifiers: [in]

`true` if a full sync should be performed. The default value is `false`.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdate Server WMI Class](sms_softwareupdate-server-wmi-class.md)
