---
title: CIEvalState Enumeration
description: In Configuration Manager, the CIEvalState enumeration is used by the ICIINFO Interface.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
