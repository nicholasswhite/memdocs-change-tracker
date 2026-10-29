---
title: CIEvalState Enumeration
description: In Configuration Manager, the CIEvalState enumeration is used by the ICIINFO Interface.
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

# CIEvalState Enumeration

In Configuration Manager, the `CIEvalState` enumeration defines configuration item evaluation states. This enumeration is used by the [ICIINFO Interface](iciinfo-interface.md).

## Syntax

```
typedef enum tagCIEvalState
{
  ciIdle = 0,
  ciEvaluating
} CIEvalState;
```

## Elements

ciIdle Configuration item is idle.

ciEvaluating Configuration item is being evaluated.

## See Also

[ICIINFO Interface](iciinfo-interface.md)
