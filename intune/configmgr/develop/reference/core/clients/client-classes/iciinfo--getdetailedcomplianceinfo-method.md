---
description: Learn how the ICIINFO::GetDetailedComplianceInfo method, in Configuration Manager, gets detailed compliance information from the last compliance evaluation run for the configuration item.
title: "ICIINFO::GetDetailedComplianceInfo Method"
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

# ICIINFO::GetDetailedComplianceInfo Method

The `ICIINFO::GetDetailedComplianceInfo` method, in Configuration Manager, gets detailed compliance information from the last compliance evaluation run for the configuration item. The string returned by the method contains an XML report from the last evaluation of the configuration item.

## Syntax

```
[IDL]
HRESULT GetDetailedComplianceInfo(
     LPWSTR* ppszComplianceInfo
);
```

#### Parameters

`ppszComplianceInfo` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to the detailed compliance information.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[ICIINFO Interface](iciinfo-interface.md)
