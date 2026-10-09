---
title: "InventoryDataContext Client WMI Class"
description: In Configuration Manager, the InventoryDataContext class is a client WMI class that represents the WMI context qualifiers to be used with inventory client agent WMI queries built from InventoryDataItem Client WMI class objects.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/68cb9039-df60-49b0-8ef8-89ad96497f63
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/725b6df3-93e8-472d-834e-e7e0d2953d35
---

# InventoryDataContext Client WMI Class

In Configuration Manager, the `InventoryDataContext` class is a client Windows Management Instrumentation (WMI) class that represents the WMI context qualifiers to be used with inventory client agent WMI queries built from [InventoryDataItem Client WMI Class](inventorydataitem-client-wmi-class.md) objects. Typically, dynamic instance providers do not require context qualifiers.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class InventoryDataContext : SMS_InventoryAgent_EmbeddedObject
{
    String Name;
    String Type;
    String Value[];
};
```

## Methods

The `InventoryDataContext` class does not define any methods.

## Properties

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [realkey]

Name of the context qualifier.

`Type` Data type: `String`

Access type: Read/Write

Qualifiers: None

String representation of the WMI variant data type for the context qualifier (for example, 3 for integer and 8200 for string array).

`Value` Data type: `String` Array

Access type: Read/Write

Qualifiers: None

Context qualifier value, consistent with the specified data type.

## Remarks

This class allows a generic method to specify context qualifiers for a WMI class query when they are needed. For example, the File System Inventory provider allows context qualifiers for specifying an amount of time to delay between back-to-back file operations. If no context qualifier is specified, there is no delay or throttling of scanning files on the system disk.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Inventory Agent Client WMI Classes](inventory-agent-client-wmi-classes.md) [InventoryDataItem Client WMI Class](inventorydataitem-client-wmi-class.md) [FileSystemFile Client WMI Class](filesystemfile-client-wmi-class.md)
