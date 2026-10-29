---
description: Learn how to use the IDCMAgentCallback interface to represent the callback for the desired configuration management agent. This interface inherits from IUnknown.
title: IDCMAgentCallback Interface
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# IDCMAgentCallback Interface

The `IDCMAgentCallback` interface, in Configuration Manager, represents the callback for the Desired Configuration Management Agent. This interface inherits from `IUnknown`.

## In This Section

The following table lists the methods in the `IDCMAgentCallback` interface.

| Term | Definition |
| --- | --- |
| [IDCMAgentCallback::NotifyComplete](idcmagentcallback--notifycomplete-method.md) | Notifies the caller that a Desired Configuration Management agent job has been completed. |
| [IDCMAgentCallback::NotifyError](idcmagentcallback--notifyerror-method.md) | Notifies the caller that a Desired Configuration Management agent job has failed to be completed. |
| [IDCMAgentCallback::NotifyProgress](idcmagentcallback--notifyprogress-method.md) | Notifies the caller of progress made on a Desired Configuration Management agent job. |

## UUID

The UUID for `IDCMAgentCallback` is 513FB8A1-67E9-4f18-8E77-0CBD6BE95708.

## See Also

[Compliance Settings (DCM) Client Interfaces](compliance-settings--dcm--client-interfaces.md)
