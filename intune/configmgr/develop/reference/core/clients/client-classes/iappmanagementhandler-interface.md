---
description: Learn how to define functions to interact with the handler in Configuration Manager using IAppManagementHandler.
title: IAppManagementHandler Interface
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# IAppManagementHandler Interface

The `IAppManagementHandler` interface, in Configuration Manager defines functions to interact with the handler.

The interface inherits from `IUnknown`.

## In This Section

The following table lists the methods in the `IAppManagementHandler` interface.

| Term | Definition |
| --- | --- |
| [IAppManagementHandler::CheckReconnectData Method](iappmanagementhandler--checkreconnectdata-method.md) | The `IAppManagementHandler::CheckReconnectData` method, in Configuration Manager, checks whether the reconnection data is valid. |
| [IAppManagementHandler::CompleteEnforcement Method](iappmanagementhandler--completeenforcement-method.md) | The `IAppManagementHandler::CompleteEnforcement` method, in Configuration Manager, completes the installation of a specific application. This method will be called only when the handler returned valid reconnection data in the EnforceApp call. |
| [IAppManagementHandler::DiscoverApp Method](iappmanagementhandler--discoverapp-method.md) | The `IAppManagementHandler::DiscoverApp` method, in Configuration Manager, runs a synchronous discovery operation for the provided synclet. |
| [IAppManagementHandler::EnforceApp Method](iappmanagementhandler--enforceapp-method.md) | The `IAppManagementHandler::EnforceApp` method, in Configuration Manager, starts the installation of a specific application. |
| [IAppManagementHandler::EnumerateApps Method](iappmanagementhandler--enumerateapps-method.md) | The `IAppManagementHandler::EnumerateApps` method, in Configuration Manager, runs a synchronous discovery operation for the provided synclet. |
| [IAppManagementHandler::GetPendingComponentList Function](iappmanagementhandler--getpendingcomponentlist-method.md) | The `IAppManagementHandler::GetPendingComponentList` method, in Configuration Manager, gets the pending component list for a specified deployment type. |

## Remarks

To obtain this interface, the application calls the `IAppManagementHandler` interface.

## UUID

The UUID for `IAppManagementHandler` is B206D835-6BD3-4e70-952E-FBA99AEBC5CE.

## See Also

[Application Management Client Interfaces](application-management-client-interfaces.md) [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
