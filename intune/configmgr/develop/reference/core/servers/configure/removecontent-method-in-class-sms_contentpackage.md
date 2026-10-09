---
description: Learn how to use the RemoteContent class method to remove the content for the given content ID from a package.
title: "RemoveContent Method in Class SMS_ContentPackage"
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

# RemoveContent Method in Class SMS_ContentPackage

The `RemoveContent` Windows Management Instrumentation (WMI) class method, in Configuration Manager, removes the content for the given content ID from the package.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 RemoveContent(
     uint32  ContentIDs[],
     boolean bRefreshDPs[],
);
```

#### Parameters

`ContentIDs` Data type: `UInt32` Array

Qualifiers: `[in, optional]`

Content identifiers for content to be removed.

`bRefreshDPs` Data type: `Boolean` Array

Qualifiers: `[in]`

`true`, if distribution points should be refreshed. The default value is `true`.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Application Server WMI Class](../../../apps/sms_application-server-wmi-class.md)
