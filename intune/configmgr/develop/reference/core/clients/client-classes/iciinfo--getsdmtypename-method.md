---
title: "ICIINFO::GetSdmTypeName Method"
description: "In Configuration Manager, the ICIINFO::GetSdmTypeName method gets the fully qualified name of a configuration item."
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ICIINFO::GetSdmTypeName Method

The `ICIINFO::GetSdmTypeName` method, in Configuration Manager, gets the fully qualified name of a configuration item.

## Syntax

```
[IDL]
HRESULT GetSdmTypeName(
     LPWSTR* ppszTypeName
);
```

#### Parameters

`ppszTypeName` Data type: `LPWSTR`

Qualifiers: [out]

Pointer to a string that represents the fully qualified name of the configuration item.

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
