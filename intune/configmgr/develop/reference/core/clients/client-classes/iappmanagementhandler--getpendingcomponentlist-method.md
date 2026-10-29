---
title: "IAppManagementHandler::GetPendingComponentList Method"
description: "The IAppManagementHandler::GetPendingComponentList method gets the pending component list for a specified deployment type."
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

# IAppManagementHandler::GetPendingComponentList Method

The `IAppManagementHandler::GetPendingComponentList` method, in Configuration Manager, gets the pending component list for a specified deployment type. This is an optional method for the application deployment type handler. It's called if the handler returns a status of "PendingUpdate" for the `EnforceApp` method. Software Center presents a list of these components to the end user, which need to be closed in order for the `EnforceApp` method to succeed.

## Syntax

```
[IDL]
HRESULT GetPendingComponentList(
     IWbemClassObject* pDeliveryTypeSynclet,
     LPWSTR* pwszPendingComponentList
);
```

#### Parameters

`pDeliveryTypeSynclet` Data type: `IWbemClassObject`

Qualifiers: [in]

The WMI object for the installation synclet which is associated with the application deployment type that is being installed.

`pwszPendingComponentList` Data type: `LPWSTR`

Qualifiers: [out]

The pending component list in XML format.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK The method succeeded. All other return values indicate failure.

E_NOTIMPL The method isn't supported by the handler.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
