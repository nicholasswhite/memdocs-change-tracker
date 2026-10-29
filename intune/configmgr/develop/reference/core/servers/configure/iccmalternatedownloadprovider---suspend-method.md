---
title: "ICcmAlternateDownloadProvider : Suspend Method"
description: "The ICcmAlternateDownloadProvider::Suspend method, in Configuration Manager, instructs the provider to suspend a given job."
ms.date: "2016-07-25T00:00:00Z"
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

# ICcmAlternateDownloadProvider : Suspend Method

The **ICcmAlternateDownloadProvider::Suspend** method, in Configuration Manager, instructs the provider to suspend a given job.

## Syntax

```
HRESULT Suspend(
            REFGUID JobID
    );

```

#### Parameters

`JobID` Data type: `REFGUID`

Qualifiers: [in]

The job on which to take action.

## Remarks

> [!NOTE]
>
> The provider must support Suspend being called on a job that is suspended. In that case, it should simply do nothing and not report an error. An error should be returned if the job is not found or if suspension failed.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK Success implies that discovery was triggered successfully. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
