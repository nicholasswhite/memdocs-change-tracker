---
description: Learn how to define application installation states in Configuration Manager using AppDetectState enumeration.
title: AppDetectState Enumeration
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# AppDetectState Enumeration

In Configuration Manager, the `AppDetectState` enumeration defines application installation states. This enumeration is used by the [IAppManagementHandler Interface](iappmanagementhandler-interface.md).

## Syntax

```
typedef enum tagAppDetectState
{
    appDetectNotFound = 0,
    appDetectInstalled,
    appDetectFailed
}AppDetectState;

```

## Elements

`appDetectNotFound` The application was not found.

`appDetectInstalled` The application is installed.

`appDetectFailed` Application detection failed.

## Remarks

This enumeration is used by the [IAppManagementHandler Interface](iappmanagementhandler-interface.md).

## See Also

[Application Management Client Interfaces](application-management-client-interfaces.md) [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
