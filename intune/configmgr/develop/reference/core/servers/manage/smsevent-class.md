---
title: SMSEvent Class
description: The SmsEvent class represents a Configuration Manager event on the client. The class implements the ICcmEvent interface.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/e453d60d-ba7e-43bc-8028-ec38e6b62512
---

# SMSEvent Class

The `SmsEvent` class represents a Configuration Manager event on the client. The class implements the `ICcmEvent` interface.

## Methods and Properties

| Term | Description |
| --- | --- |
| [ICcmEvent::EventType Property](iccmevent--eventtype-property.md) | Indicates the type of Windows Management Instrumentation (WMI) event that is being raised. |
| [ICcmEvent::RawEvent Property](iccmevent--rawevent-property.md) | Adds information to custom events. |
| [ICcmEvent::SetProperty Method](iccmevent--setproperty-method.md) | Sets an event property. |
| [ICcmEvent::Submit Method](iccmevent--submit-method.md) | Submits an event to WMI. |
| [ICcmEvent::SubmitPending Method](iccmevent--submitpending-method.md) | Submits an event to WMI in situations where the Configuration Manager Agent Host (CCMEXEC) service might not be running. |

## Remarks

The `ProgID` for the automation object is Microsoft.SMS.Event and it is implemented as part of Smscore.dll. The Visual Basic reference for early binding is SMSCorLib. The early binding object name is `SMSEvent`.

## Requirements

smscore.dll

### Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
