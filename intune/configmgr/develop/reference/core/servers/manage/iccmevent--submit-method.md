---
title: "ICCMEvent::Submit Method"
description: In Configuration Manager, the ICCMEvent::Submit method submits an event to Windows Management Instrumentation.
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

# ICCMEvent::Submit Method

In Configuration Manager, the `ICcmEvent::Submit` method submits an event to Windows Management Instrumentation (WMI).

## Syntax

```
[C++]
HRESULT ICcmEvent::Submit();
```

#### Parameters

None.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded.

## Requirements

Smscore.dll.

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMSEvent Class (client)](smsevent-class.md)
