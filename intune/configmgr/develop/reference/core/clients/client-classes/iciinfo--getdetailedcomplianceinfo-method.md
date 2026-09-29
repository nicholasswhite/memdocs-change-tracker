---
description: Learn how the ICIINFO::GetDetailedComplianceInfo method, in Configuration Manager, gets detailed compliance information from the last compliance evaluation run for the configuration item.
title: "ICIINFO::GetDetailedComplianceInfo Method"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
