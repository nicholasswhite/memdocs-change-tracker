---
description: Learn how to represent application actions using CCM_ApplicationActions class in Configuration Manager.
title: "CCM_ApplicationActions Client WMI Class"
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

# CCM_ApplicationActions Client WMI Class

The `CCM_ApplicationActions` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents application actions.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_ApplicationActions :
{
    DateTime NextGlobalRevalTime;
    DateTime NextRetryTime;
    DateTime NextServiceWindowTime;
};
```

## Methods

The `CCM_ApplicationActions` class does not define any methods.

## Properties

`NextGlobalRevalTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Next global reevaluation time.

`NextRetryTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Next retry time

`NextServiceWindowTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

Next service window time.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
