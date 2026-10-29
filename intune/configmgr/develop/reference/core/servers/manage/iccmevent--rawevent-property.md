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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
