---
title: "ICIINFO::GetDependantPackages Method"
description: The ICIINFO::GetDependantPackages method, in Configuration Manager, gets the dependent package information for the configuration item.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ICIINFO::GetDependantPackages Method

The `ICIINFO::GetDependantPackages` method, in Configuration Manager, gets the dependent package information for the configuration item.

## Syntax

```
[IDL]
HRESULT GetDependantPackages(
     ULONG* pulNumDependants,
     struct CIPackageInfo** ppInfo
);
```

#### Parameters

`pulNumDependants` Data type: `ULONG`

Qualifiers: [out]

Pointer to the number of dependent packages.

`ppInfo` Data type: `CIPackageInfo`

Qualifiers: [out]

Pointer to a pointer to one [CIPackageInfo Structure](cipackageinfo-structure.md) for each dependent package.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following:

S_OK The method succeeded. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[ICIINFO Interface](iciinfo-interface.md) [CIPackageInfo Structure](cipackageinfo-structure.md)
