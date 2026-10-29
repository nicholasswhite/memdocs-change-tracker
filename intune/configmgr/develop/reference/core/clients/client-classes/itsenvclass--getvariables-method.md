---
title: "ITSEnvClass::GetVariables Method"
description: In Configuration Manager, the GetVariables method gets the variables for the operating system deployment task sequence environment.
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
