---
description: Learn how to exclude scan paths from all members in a specified collection using the ExcludeScanPaths class method in Configuration Manager.
title: "ExcludeScanPaths Method in Class SMS_ClientOperation"
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

# ExcludeScanPaths Method in Class SMS_ClientOperation

The `ExcludeScanPaths` Windows Management Instrumentation (WMI) class method in Configuration Manager that excludes scan paths from all members in specified collection.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 ExcludeScanPaths
{
    [IN]    UInt64 ThreatID
    [IN]    String ExclusionSettingsUniqueID
    [IN]    String ExcludedPaths[]
    [IN]    String TargetCollectionID
    [OUT]   UInt32 OperationID
};
```

## Parameters

`ThreatID` Data type: `UInt64`

Qualifiers: [id("0"), in]

ThreatID.

`ExclusionSettingsUniqueID` Data type: `String`

Qualifiers: [id("1"), in]

ExclusionSettingsUniqueID.

`ExcludedPaths` Data type: `String Array`

Qualifiers: [id("2"), in]

ExcludedPaths.

`TargetCollectionID` Data type: `String`

Qualifiers: [id("3"), in]

TargetCollectionID.

`OperationID` Data type: `UInt32`

Qualifiers: [id("4"), out]

OperationID.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
