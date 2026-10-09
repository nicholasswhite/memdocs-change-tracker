---
title: "ICCMEvent::RawEvent Property"
description: "In Configuration Manager, ICcmEvent::RawEvent is a read-only property that indicates information to add to a raw event."
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

# ICCMEvent::RawEvent Property

`ICcmEvent::RawEvent` is a read-only property in Configuration Manager that indicates information to add to a raw event.

## Syntax

```
[C++]
HRESULT ICcmEvent::RawEvent([out, retval] IUnknown** ppWmiEvent);
```

#### Parameters

`ppWmiEvent` Data type: `IUnknown`

Qualifiers: [out, retval]

Pointer to a pointer to the `IUnknown` interface of the internal Windows Management Instrumentation (WMI) event.

## Return Values

The property returns an `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK The method succeeded.

## Remarks

Use of this property permits information that can't be added through the [SetProperty method](iccmevent--setproperty-method.md) method to be added to custom events.

This property is recommended only for advanced users who need to add information to custom events that can't be accomplished through the [SetProperty method](iccmevent--setproperty-method.md) method. It isn't supported in VBScript.

## Requirements

Smscore.dll.

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMSEvent Class (client)](smsevent-class.md)
