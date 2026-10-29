---
description: "Learn how to run a synchronous discovery operation for the provided synclet using IAppManagementHandler::DiscoveryApp."
title: "IAppManagementHandler::DiscoverApp Method"
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

# IAppManagementHandler::DiscoverApp Method

The `IAppManagementHandler::DiscoverApp` method, in Configuration Manager, runs a synchronous discovery operation for the provided synclet.

## Syntax

```
[IDL]
HRESULT DiscoverApp(
     HANDLE hUserToken,
     LPCWSTR szDeploymentTypeId,
     DWORD dwDeploymentTypeRevision,
     AppDeploymentTypeData* pDetectResult
);
```

#### Parameters

`hUserToken` Data type: `HANDLE`

Qualifiers: [in]

The user token. If it's null, the action is for computer. If it isn't NULL, the action is for the user.

`szDeploymentTypeId` Data type: `DWORD`

Qualifiers: [in]

.

`dwDeploymentTypeRevision` Data type: `DWORD`

Qualifiers: [in]

.

`pDetectResult` Data type: `AppDeploymentTypeData`

Qualifiers: [out]

.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK Success implies that discovery was triggered successfully. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[IAppManagementHandler Interface](iappmanagementhandler-interface.md) [Application Management Client Interfaces](application-management-client-interfaces.md) [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
