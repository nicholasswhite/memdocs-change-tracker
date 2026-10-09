---
title: "IsOfficeContent Method in Class SMS_Content"
description: Learn about the IsOfficeContent class method. In Configuration Manager, this method specifies whether content is Microsoft 365 content.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/1dd701e0-441f-4b0a-9806-aa47decc4e35
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/0a2fc935-5977-4aa6-9f55-0be03bd2acb8
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# IsOfficeContent Method in Class SMS_Content

The `IsOfficeContent` Windows Management Instrumentation (WMI) class method, in Configuration Manager, specifies whether content is Microsoft 365 content.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
Boolean IsOfficeContent (
    UInt32 ContentId
);

```

#### Parameters

`ContentId` Data type: `UInt32`

Qualifiers: [in]

Content ID.

## Return Values

`True` if content is Microsoft 365 content; otherwise, `False`.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_Content server WMI class](sms_content-server-wmi-class.md)
