---
title: "ITSEnvClass::GetVariables Method"
description: In Configuration Manager, the GetVariables method gets the variables for the operating system deployment task sequence environment.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ITSEnvClass::GetVariables Method

In Configuration Manager, the `GetVariables` method gets the variables for the operating system deployment task sequence environment.

## Syntax

```
[IDL]
HRESULT GetVariables(
     VARIANT* variables
);
```

#### Parameters

`variables` Data type: `VARIANT`

Qualifiers: [out, retval]

Pointer to the environment variables.

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following value.

S_OK The method succeeded.

## See Also

[ITSEnvClass Interface](itsenvclass-interface.md)
