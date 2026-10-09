---
description: ICcmEvent::EventType is a read/write property in Configuration Manager that indicates the type of Windows Management Instrumentation event that is being raised.
title: "ICCMEvent::EventType Property"
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

# ICCMEvent::EventType Property

`ICcmEvent::EventType` is a read/write property in Configuration Manager that indicates the type of Windows Management Instrumentation (WMI) event that is being raised.

## Syntax

```
[C++]
HRESULT ICcmEvent::EventType([out, retval] BSTR* sEventType);

HRESULT ICcmEvent::EventType([in] BSTR sEventType);
```

#### Parameters

`sEventType` Data type: `BSTR`

Qualifiers: [in, out, retval]

On input, the value to set for the event type. On output, this parameter points to the retrieved event type.

## Return Values

The property returns an `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK The method succeeded.

## Remarks

This property must correspond to an `ICcmEvent`-derived class registered in the root\ccm\events namespace.

## Requirements

Smscore.dll.

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMSEvent Class (client)](smsevent-class.md)
