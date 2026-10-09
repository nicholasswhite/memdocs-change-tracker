---
title: "SMS_DmInvVersion Client WMI Class"
description: In Configuration Manager, The SMS_DmInvVersion class is a client Windows Management Instrumentation class that represents the device management inventory version.
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

# SMS_DmInvVersion Client WMI Class

The `SMS_DmInvVersion` class is a client Windows Management Instrumentation (WMI) class in Configuration Manager that represents the device management inventory version.

## Syntax

```
Class SMS_DmInvVersion
{
   UInt32 Version
};
```

## Methods

The `SMS_ActiveSyncConnectedDevice` class doesn't define any methods.

## Properties

`Version` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The inventory version.

## See Also

[Device Management Client WMI Classes](device-management-client-wmi-classes.md)
