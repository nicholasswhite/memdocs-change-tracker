---
description: Article detailing how to use CCM_ServiceWindowManager in Configuration Manager to manage service windows on the client computer.
title: "CCM_ServiceWindowManager Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CCM_ServiceWindowManager Client WMI Class

The `CCM_ServiceWindowManager` WMI class is a client class, in Configuration Manager, manages service windows on the client computer.

The following syntax is simplified from the Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
class CCM_ServiceWindowManager();
```

## Methods

The following table shows the methods in the `CCM_ServiceWindowManager` class.

| Method | Description |
| --- | --- |
| [GetCurrentWindowAvailableTime Method in Class CCM_SoftwareUpdatesManager](getcurrentwindowavailabletime-method-in-class-ccm_servicewindowmanager.md) | Gets the time remaining in a currently-active service window for a specified type. |
| [GetNextServiceWindowID Method in Class CCM_SoftwareUpdatesManager](getnextservicewindowid-method-in-class-ccm_servicewindowmanager.md) | Gets the identifier of the next service window closest to the current time. |
| [IsFutureWindowAvailable Method in Class CCM_SoftwareUpdatesManager](isfuturewindowavailable-method-in-class-ccm_servicewindowmanager.md) | Determines whether a service window of a specified type and a given duration is going to be available. |
| [IsWindowAvailableNow Method in Class CCM_SoftwareUpdatesManager](iswindowavailablenow-method-in-class-ccm_servicewindowmanager.md) | Determines whether a service window of a specified type and a given duration is available to run at the point of time when the call is made. |

## Properties

The `CCM_ServiceWindowManager` class does not define any properties.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
