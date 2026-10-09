---
title: "SMS_DPGroupPackages Server WMI Class"
description: The SMS_DPGroupPackages WMI class is an SMS Provider server class that represents distribution point packages.
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

# SMS_DPGroupPackages Server WMI Class

The `SMS_DPGroupPackages` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents distribution point packages.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DPGroupPackages : SMS_BaseClass
{
    String GroupID;
    String PkgID;
};
```

## Methods

The `SMS_DPGroupPackages` class does not define any methods.

## Properties

`GroupID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique identifier for the distribution point group.

`PkgID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Package associated with the distribution point group.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
