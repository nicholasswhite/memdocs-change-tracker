---
title: AppAction Enumeration
description: Learn how the AppAction enumeration defines action types.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
