---
title: "CCM_PowerManagementClientOptoutSetting Client WMI Class"
description: In Configuration Manager, the CCM_PowerManagementClientOptoutSetting Windows Management Instrumentation class is an SMS Provider server class that represents the settings that allow users to exclude their device from power management.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# CCM_PowerManagementClientOptoutSetting Client WMI Class

The `CCM_PowerManagementClientOptoutSetting` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the settings that allow users to exclude their device from power management.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_PowerManagementClientOptoutSetting :
{
    Boolean AdminAllowOptout;
    Boolean EffectiveClientOptOut;
    Boolean IsClientOptOut;
};
```

## Methods

The `CCM_PowerManagementClientOptoutSetting` class does not define any methods.

## Properties

`AdminAllowOptOut` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the Admin allows users to exclude their device from power management.

`EffectiveClientOptOut` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the result of AdminAllowOptOut and IsClientOptOut is ClientOptOut.

`IsClientOptOut` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the user has excluded their device from power management.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
