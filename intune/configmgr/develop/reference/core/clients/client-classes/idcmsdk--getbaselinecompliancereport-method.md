---
description: "Learn how to use the IDCMSDK::GetBaselineComplianceReport method to retrieve the cached discovery report for the specified configuration item baseline."
title: "IDCMSDK::GetBaselineComplianceReport Method"
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

# IDCMSDK::GetBaselineComplianceReport Method

The `IDCMSDK::GetBaselineComplianceReport` method, in Configuration Manager, retrieves the cached discovery report for the specified configuration item baseline.

## Syntax

```
[IDL]
HRESULT GetBaselineComplianceReport(
     LPCWSTR  pszId,
     LPCWSTR  pszVersion,
     LPWSTR*  ppszComplianceInfo
);
```

#### Parameters

`pszId` Data type: `LPCWSTR`

Qualifiers: [in]

Pointer to a null-terminated string specifying the ID of the baseline configuration item. An example ID is "ScopeId_6CD81FFE-63C4-4AF6-B50A-0847707628A0/Baseline_780a1633-ba4d-4172-b2b1-583cc733ef56".

`pszVersion` Data type: `LPCWSTR`

Qualifiers: [in, unique]

Pointer to a null-terminated string specifying the baseline configuration item version. If this parameter is set to `null`, the method retrieves the latest version of the baseline configuration item that exists in the client data store.

`ppszComplianceInfo` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to a null-terminated string specifying a report of compliance information for the baseline configuration item.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[IDCMSDK Interface](idcmsdk-interface.md)
