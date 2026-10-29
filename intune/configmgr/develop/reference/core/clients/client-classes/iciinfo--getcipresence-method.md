---
title: "ICIINFO::GetCIPresence Method"
description: "In Configuration Manager, the ICIINFO::GetCIPresence method gets the current presence for the configuration item, including the compliance state for the configuration item."
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

# ICIINFO::GetCIPresence Method

The `ICIINFO::GetCIPresence` method, in Configuration Manager, gets the current presence for the configuration item. The presence data includes the compliance state for the configuration item.

## Syntax

```
[IDL]
HRESULT GetCIPresence(
     CIPresence* pCIPresence
);
```

#### Parameters

`pCIPresence` Data type: `CIPresence`

Qualifiers: [out]

Pointer to a [CIPresence Enumeration](cipresence-enumeration.md) value indicating the current presence for the configuration item.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[ICIINFO Interface](iciinfo-interface.md) [CIPresence Enumeration](cipresence-enumeration.md)
