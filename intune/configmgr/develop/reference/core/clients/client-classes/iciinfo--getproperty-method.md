---
title: "ICIINFO::GetProperty Method"
description: Learn how the ICIINFO::GetProperty method, in Configuration Manager, gets a named property value from the configuration item.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# ICIINFO::GetProperty Method

The `ICIINFO::GetProperty` method, in Configuration Manager, gets a named property value from the configuration item.

## Syntax

```
[IDL]
HRESULT GetProperty(
     LanguageId* pLanguageId,
     LPCWSTR pszPropName,
     LPWSTR* ppszPropValue
);
```

#### Parameters

`pLanguageId` Data type: `LanguageId`

Qualifiers: [in, out]

Pointer to the language ID that is used to obtain the property. If there's no localized name for this ID, the method attempts to obtain the language-independent version of the property. If this doesn't exist, the method returns an error. On successful return from the method, this parameter indicates the language ID for the property retrieved.

`pszPropName` Data type: `LPCWSTR`

Qualifiers: [in]

Pointer to a null-terminated string specifying the name of the property.

`ppszPropValue` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to a null-terminated string specifying the property value.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[ICIINFO Interface](iciinfo-interface.md)
