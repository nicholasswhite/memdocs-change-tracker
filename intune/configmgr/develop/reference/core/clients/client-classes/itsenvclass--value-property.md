---
title: "ITSEnvClass::Value Property"
description: In Configuration Manager, the Value property contains the value of an operating system deployment task sequence environment variable.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# ITSEnvClass::Value Property

In Configuration Manager, the `Value` property contains the value of an operating system deployment task sequence environment variable.

## Syntax

```
[IDL]
HRESULT Value([in] BSTR Name, [in] BSTR Value);

HRESULT Value([in] BSTR Name, [out,retval] BSTR* Value);
```

#### Parameters

`Name` Data type: `BSTR`

Qualifiers: [in]

The name of the environment variable.

`Value` Data type: `BSTR`

Qualifiers: [in; out, retval]

On input, the value to set for the environment variable. On output, this parameter points to the value that is retrieved for the supplied name.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following value.

S_OK The method succeeded.

## Remarks

The `get_Value` function succeeds with S_OK when called with an invalid variable name, but retrieves an empty string for the value. This behavior differs from the more common return of a non-zero exit code to indicate an invalid variable name input.

## See Also

[ITSEnvClass Interface](itsenvclass-interface.md)
