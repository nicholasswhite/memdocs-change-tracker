---
description: "Learn how to use the ICIINFO::GetCategoryCount method to get the count of categories that are associated with the configuration item."
title: "ICIINFO::GetCategoryCount Method"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ICIINFO::GetCategoryCount Method

The `ICIINFO::GetCategoryCount` method, in Configuration Manager, gets the count of categories that are associated with the configuration item.

## Syntax

```
[IDL]
HRESULT GetCategoryCount(
     ULONG* pulCount
);
```

#### Parameters

`pulCount` Data type: `ULONG`

Qualifiers: [out]

Pointer to the count of categories applied to the configuration item.

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
