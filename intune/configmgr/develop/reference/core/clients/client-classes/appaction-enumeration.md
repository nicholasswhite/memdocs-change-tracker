---
title: AppAction Enumeration
description: Learn how the AppAction enumeration defines action types.
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

# AppAction Enumeration

In Configuration Manager, the `AppAction` enumeration defines action types. This enumeration is used by the [IAppManagmentTypes Interface](iappmanagementtypes-interface.md).

## Syntax

```
typedef enum AppAction
{
    appDiscovery = 0,
    appInstall = 1,
    appUninstall = 2
}AppAction;
```

## Elements

`appDiscovery` The action type is discovery.

`appInstall` The action type is install.

`appUninstall` The action type is uninstall.

## See Also

[IAppManagementTypes Interface](iappmanagementtypes-interface.md) [Application Management Client Interfaces](application-management-client-interfaces.md) [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
