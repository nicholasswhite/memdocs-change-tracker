---
title: InventoryActionStatus Client WMI Class
description: The InventoryActionStatus class is a client Windows Management Instrumentation (WMI) class that defines the status of an inventory action.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# InventoryActionStatus Client WMI Class

In Configuration Manager, the `InventoryActionStatus` class is a client Windows Management Instrumentation (WMI) class that defines the status of an inventory action.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class InventoryActionStatus
{
      String InventoryActionID;
      DateTime LastCycleStartedDate;
      UInt32 LastMajorReportVersion;
      UInt32 LastMinorReportVersion;
      DateTime LastReportDate;
};
```

## Methods

The `InventoryActionStatus` class does not define any methods.

## Properties

`InventoryActionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The inventory action ID.

`LastCycleStartedDate` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

The time when the last inventory cycle started.

`LastMajorReportVersion` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The major version of the last major report.

`LastMinorReportVersion` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The minor version on the last report.

`LastReportDate` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

The date and time of the last report.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Inventory Agent Client WMI Classes](inventory-agent-client-wmi-classes.md)
