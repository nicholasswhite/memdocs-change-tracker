---
title: "ICIINFO::GetCategory Method"
description: "The ICIINFO::GetCategory method gets a localized category name by index and the group name of the category."
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

# ICIINFO::GetCategory Method

The `ICIINFO::GetCategory` method, in Configuration Manager, gets a localized category name by index and the group name of the category.

## Syntax

```
[IDL]
HRESULT GetCategory(
     ULONG ulIndex,
     LanguageId* pLanguageId,
     LPWSTR* ppszCategoryGroup,
     LPWSTR* ppszCategoryName
);
```

#### Parameters

`ulIndex` Data type: `ULONG`

Qualifiers: [in]

Index of the category to retrieve.

`pLanguageId` Data type: `LanguageId`

Qualifiers: [in, out]

Pointer to a language ID used to obtain the localized category name. If there is no localized name for this ID, the method attempts to obtain the language-independent string. If this does not exist, the method returns an error. On successful return from the method, this parameter indicates the language ID for the localized category name.

`ppszCategoryGroup` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to the category group.

`ppszCategoryName` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to the localized name of the category.

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
