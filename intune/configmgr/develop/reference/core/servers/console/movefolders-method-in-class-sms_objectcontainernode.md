---
title: "MoveFolders Method in Class SMS_ObjectContainerNode"
description: Learn how the MoveFolders Windows Management (WMI) class method, in Configuration Manager, moves folders to another folder location.
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

# MoveFolders Method in Class SMS_ObjectContainerNode

The `MoveFolders` Windows Management (WMI) class method, in Configuration Manager, moves folders to another folder location.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 MoveFolders(
      UInt32 ContainerNodeIDs[],
      UInt32 TargetContainerNodeID,
);
```

#### Parameters

`ContainerNodeIDs` Data type: `UInt32` Array

Qualifiers: [in]

IDs of the folders, or nodes, to move.

`TargetContainerNodeID` Data type: `UInt32`

Qualifiers: [in]

The ID for the destination folder, or node.

## Return Value

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ObjectContainerNode Server WMI Class](sms_objectcontainernode-server-wmi-class.md)
