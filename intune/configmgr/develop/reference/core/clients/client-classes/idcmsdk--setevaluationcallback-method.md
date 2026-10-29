---
title: "IDCMSDK::SetEvaluationCallback Method"
description: "In Configuration Manager, the IDCMSDK::SetEvaluationCallback method associates a callback object with an existing evaluation job specified by job ID."
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

# IDCMSDK::SetEvaluationCallback Method

The `IDCMSDK::SetEvaluationCallback` method, in Configuration Manager, associates a callback object with an existing evaluation job, specified by job ID.

## Syntax

```
[IDL]
HRESULT SetEvaluationCallback(
     JobIdRef  jobId,
     IDCMAgentCallback*  pCallback
);
```

#### Parameters

`jobId` Data type: `JobIdRef`

Qualifiers: [in]

ID of the evaluation job to retrieve.

`pCallback` Data type: `IDCMAgentCallback`

Qualifiers: [in]

Pointer to an [IDCMAgentCallback Interface](idcmagentcallback-interface.md) object. This parameter can be set to `null` if no callback is available.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded. All other return values indicate failure.

## Remarks

The typical way to use this method is to pass `null` for the `pCallback` parameter.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[IDCMSDK Interface](idcmsdk-interface.md) [IDCMAgentCallback Interface](idcmagentcallback-interface.md)
