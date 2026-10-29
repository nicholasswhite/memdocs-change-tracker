---
title: IDCMSDK Interface
description: The interface represents the Desired Configuration Management SDK and defines methods used to perform operations on baseline configuration items.
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

# IDCMSDK Interface

The `IDCMSDK` interface, in Configuration Manager, represents the Desired Configuration Management SDK and defines methods used to perform operations on baseline configuration items. The interface inherits from `IDispatch`.

## In This Section

The following table lists the methods in the `IDCMSDK` interface.

| Method | Description |
| --- | --- |
| [IDCMSDK::EvaluateBaseline](idcmsdk--evaluatebaseline-method.md) | Runs discover operation for the provided configuration item ID. |
| [IDCMSDK::GetAssignedBaselines](idcmsdk--getassignedbaselines-method.md) | Retrieves the assigned baseline configuration items. |
| [IDCMSDK::GetBaselineComplianceReport](idcmsdk--getbaselinecompliancereport-method.md) | Retrieves the cached discovery report for the specified configuration item baseline. |
| [IDCMSDK::GetBaselineInfo](idcmsdk--getbaselineinfo-method.md) | Retrieves the configuration item information for the specified configuration item baseline. |
| [IDCMSDK::SetEvaluationCallback](idcmsdk--setevaluationcallback-method.md) | Retrieves an existing evaluation job by ID. |

## UUID

The UUID for `IDCMSDK` is 08595CA8-6A42-4ce1-A1D6-8B6C2811A555.

## See Also

[Compliance Settings (DCM) Client Interfaces](compliance-settings--dcm--client-interfaces.md) [IDCMAgentCallback Interface](idcmagentcallback-interface.md)
