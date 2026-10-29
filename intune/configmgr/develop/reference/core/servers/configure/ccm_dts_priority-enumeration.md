---
title: CCM_DTS_PRIORITY enumeration
description: The CCM_DTS_PRIORITY enumeration indicates the priority of the download.
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

# CCM_DTS_PRIORITY enumeration

The **CCM_DTS_PRIORITY** enumeration indicates the priority of the download.

## Syntax

```
typedef enum
{
    CCM_DTS_PRIORITY_FOREGROUND,
    CCM_DTS_PRIORITY_HIGH,
    CCM_DTS_PRIORITY_NORMAL,
    CCM_DTS_PRIORITY_LOW,
}CCM_DTS_PRIORITY;

```

## Members

| Priority flag | Description |
| --- | --- |
| CCM_DTS_PRIORITY_FOREGROUND | The highest priority. |
| CCM_DTS_PRIORITY_HIGH | High priority. |
| CCM_DTS_PRIORITY_NORMAL | Normal priority. |
| CCM_DTS_PRIORITY_LOW | Low priority. |

## Remarks

The only strict requirement is that jobs at a lower priority do not block progress of jobs at a higher priority. Providers must respect this.

## Requirements

### Runtime requirements

For more information, see [Configuration Manager client runtime requirements](../../../../core/reqs/client-runtime-requirements.md).

### Development requirements

For more information, see [Configuration Manager client development requirements](../../../../core/reqs/client-development-requirements.md).
