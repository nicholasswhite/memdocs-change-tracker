---
title: CCM_DTS_FLAG Enumeration
description: The CCM_DTS_FLAG enumeration indicates special options on download jobs.
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

# CCM_DTS_FLAG Enumeration

The **CCM_DTS_FLAG** enumeration indicates special options on download jobs.

## Syntax

```
typedef enum
{
    CCM_DTS_FLAG_SINGLEFILE             = 0x00000001,
    CCM_DTS_FLAG_DIRECTORY              = 0x00000002,
    CCM_DTS_FLAG_NOTIFYPROGRESS         = 0x00000004,
    CCM_DTS_FLAG_INSECURETRANSPORT      = 0x00000008,
    CCM_DTS_FLAG_TOPLEVELFILESONLY      = 0x00000010,
    CCM_DTS_FLAG_SENDAUTHHEADERS        = 0x00000020,
    CCM_DTS_FLAG_SENDAUTHHEADERS_MIXED  = 0x00000040,
    CCM_DTS_FLAG_USEINPUTMANIFEST       = 0x00000080,
    CCM_DTS_FLAG_SKIPHOSTCHANGEHANDLING = 0x00000100
}
CCM_DTS_FLAG;

```

## Members

| CTS flag | Description |
| --- | --- |
| CCM_DTS_FLAG_SINGLEFILE | Reserved. |
| CCM_DTS_FLAG_DIRECTORY | Indicates that `szRemotePath` is a directory and that all of its contents should be downloaded. This should always be specified in the case of alternate providers. |
| CCM_DTS_FLAG_NOTIFYPROGRESS | This indicates that progress notifications are required. Even if this flag is not specified, success and error notifications are still required. |
| CCM_DTS_FLAG_INSECURETRANSPORT | Reserved. |
| CCM_DTS_FLAG_TOPLEVELFILESONLY | Reserved. |
| CCM_DTS_FLAG_SENDAUTHHEADERS | Reserved. |
| CCM_DTS_FLAG_SENDAUTHHEADERS_MIXED | Reserved. |
| CCM_DTS_FLAG_USEINPUTMANIFEST | Reserved. |
| CCM_DTS_FLAG_SKIPHOSTCHANGEHANDLING | Reserved. |

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
