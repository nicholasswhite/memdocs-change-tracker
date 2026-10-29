---
title: CCM_CONTENTFLAG Enumeration
description: Learn about the CCM_CONTENTFLAG Enumeration that contains options for transferring content.
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

# CCM_CONTENTFLAG Enumeration

The **CCM_CONTENTFLAG** enumeration contains options for transferring content.

## Syntax

```vb
typedef enum
{
    CCM_CONTENTFLAG_LOCAL_ONLY                  = 0x00000001,
    CCM_CONTENTFLAG_REMOTE_ONLY                 = 0x00000002,
    CCM_CONTENTFLAG_LOCAL_OR_REMOTE             = 0x00000004,
    CCM_CONTENTFLAG_PROTECTED_ONLY              = 0x00000008,
    CCM_CONTENTFLAG_ALLOW_CACHING               = 0x00000010,
    CCM_CONTENTFLAG_PEERDP                      = 0x00000020,
    CCM_CONTENTFLAG_REMOTE_NOLOCALPEERDP        = 0x00000040,
    CCM_CONTENTFLAG_DELTA_DOWNLOAD              = 0x00000080,
    CCM_CONTENTFLAG_ALLOW_ALTERNATE_PROVIDERS   = 0x00000100
}
CCM_CONTENTFLAG;
```

## Members

| Content flag | Description |
| --- | --- |
| CCM_CONTENTFLAG_LOCAL_ONLY | Local only. |
| CCM_CONTENTFLAG_REMOTE_ONLY | Remote only. |
| CCM_CONTENTFLAG_LOCAL_OR_REMOTE | Local or remote. |
| CCM_CONTENTFLAG_PROTECTED_ONLY | Protected only. |
| CCM_CONTENTFLAG_ALLOW_CACHING | Allow caching. |
| CCM_CONTENTFLAG_PEERDP | Branch distribution point. |
| CCM_CONTENTFLAG_REMOTE_NOLOCALPEERDP | No local branch distribution point. |
| CCM_CONTENTFLAG_DELTA_DOWNLOAD | Delta download. |
| CCM_CONTENTFLAG_ALLOW_ALTERNATE_PROVIDERS | Allow alternate providers. |

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
