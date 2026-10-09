---
description: Learn how to represent a pending re-registration at the time of site reassignment in Configuration Manager.
title: "SMS_PendingReRegistrationOnSiteReAssignment Client WMI Class"
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

# SMS_PendingReRegistrationOnSiteReAssignment Client WMI Class

> [!IMPORTANT]
>
> This class supports the Configuration Manager 2007 infrastructure and is not intended to be used directly from your code.

The `SMS_PendingReRegistrationOnSiteReAssignment` class is a client Windows Management Instrumentation (WMI) class, in Configuration Manager, that represents a pending re-registration at the time of site reassignment.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_PendingReRegistrationOnSiteReAssignment
{
      UInt32 Flags;
      String LastAssignedSite;
      String NewAssignedSite;
};
```

## Methods

The `SMS_PendingReRegistrationOnSiteReAssignment` class does not define any methods.

## Properties

`Flags` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Flags defining options for the pending re-registration.

`LastAssignedSite` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site code of the last site that was assigned.

`NewAssignedSite` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site code of the new site being assigned.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
