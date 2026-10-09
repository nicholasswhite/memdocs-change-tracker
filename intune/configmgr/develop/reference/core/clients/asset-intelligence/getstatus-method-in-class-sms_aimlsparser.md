---
title: "GetStatus Method in Class SMS_AIMLSParser"
description: The GetStatus Windows Management Instrumentation (WMI) class method is used to monitor the status of a previous call to the Import method.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# GetStatus Method in Class SMS_AIMLSParser

The `GetStatus` Windows Management Instrumentation (WMI) class method, in Configuration Manager, which is used to monitor the status of a previous call to the `Import` method.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetStatus(
     SInt32 Status
);
```

#### Parameters

`Status` Data type: `SInt32`

Qualifiers: [out]

When 0, indicates a successful call to `Import`.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_AIMLSParser Server WMI Class](sms_aimlsparser-server-wmi-class.md)
