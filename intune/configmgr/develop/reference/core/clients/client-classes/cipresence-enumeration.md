---
description: Learn how to define configuration item presence types used in the discovery process with CIPresence enumeration.
title: CIPresence Enumeration
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

# CIPresence Enumeration

In Configuration Manager, the `CIPresence` enumeration defines configuration item presence types used in the discovery process.

## Syntax

```
typedef enum tagCIPresence
{
  ciNotPresent = 0,ciNonCompliant = 0,
  ciPresent = 1,ciCompliant = 1,
  ciNotApplicable = 2,
  ciPresenceUnknown = 3,ciComplianceUnknown = 3,
  ciEvaluationError = 4,
  ciNotEvaluated = 5
} CIPresence;
```

## Elements

`ciNotPresent, ciNonCompliant` Configuration item not present or not compliant.

`ciPresent, ciCompliant` Configuration item present or compliant.

`ciNotApplicable` Configuration item not applicable.

`ciPresenceUnknown, ciComplianceUnknown` Configuration item presence or compliance unknown.

`ciEvaluationError` Configuration item evaluation error.

`ciNotEvaluated` Configuration item not evaluated.

## Remarks

This enumeration is used by the [ICIINFO Interface](iciinfo-interface.md).

## See Also

[ICIINFO Interface](iciinfo-interface.md)
