---
title: "Reference for Intune Management Extensions"
description: Reference topic for the IntuneManagementExtension Entity category of entity collections in the Intune Data Warehouse API.
ms.date: "2024-10-30T00:00:00Z"
ms.topic: reference
author: nicholasswhite
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: nwhite
ms.collection: M365-identity-device-management
ms.reviewer: jamiesil
ms.service: microsoft-intune
ms.subservice: developer
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Reference for Intune Management Extensions

The **intuneManagementExtensions** category contains entities for mobile devices that track information such as:

- Versions of an IntuneManagementExtension
- Installation status of an IntuneManagementExtension

## intuneManagementExtensionVersions

The **intuneManagementExtensionVersion** entity lists all the versions used by intuneManagementExtensions.

| Property | Description | Example |
| --- | --- | --- |
| extensionVersionKey | Unique identifier of the intuneManagementExtensions version. | 1 |
| extensionVersion | The 4 digit version number. | 1.0.2.0 |

## intuneManagementExtensionHealthStates

The **intuneManagementExtensionHealthState** lists all possible health states of the intuneManagementExtensions.

| Property | Description | Example |
| --- | --- | --- |
| extensionStateKey | Unique identifier of health state. | 2 |
| extensionState | Health state of a IntuneManagementExtension. | Healthy |

## intuneManagementExtensions

The **intuneManagementExtension** lists the IntuneManagementExtensions health on each Windows 10 device per day. The data is retained for the last 60 days.

| Property | Description | Example |
| --- | --- | --- |
| dateKey | Unique identifier of the Date. | 123 |
| tenantKey | Unique identifier of the Tenant. | 456 |
| deviceKey | Unique identifier of the Device. | 789 |
| extensionVersionKey | Unique identifier of the intuneManagementExtension version. | 1 |
| extensionStateKey | Unique identifier of health state. | 2 |
