---
title: "CCM_InstalledDeploymentType Client WMI Class"
description: In Configuration Manager, the CCM_InstalledDeploymentType Windows Management Instrumentation class is an SMS Provider server class that represents an installed deployment type.
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

# CCM_InstalledDeploymentType Client WMI Class

The `CCM_InstalledDeploymentType` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents an installed deployment type.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_InstalledDeploymentType :
{
    String Id;
    String Revision;
};
```

## Methods

The `CCM_InstalledDeploymentType` class does not define any methods.

## Properties

`Id` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier.

`Revision` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Revision.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
