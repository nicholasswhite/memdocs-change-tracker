---
title: "GetClientsCountByCollections Method in Class SMS_MigrationCollectionInfo"
description: A Windows Management Instrumentation class method that retrieves the number of clients in the specified collections.
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

# GetClientsCountByCollections Method in Class SMS_MigrationCollectionInfo

The `GetClientsCountByCollections` Windows Management Instrumentation (WMI) class method, in Configuration Manager, retrieves the number of clients in the specified collections.

> [!NOTE]
>
> This method is reserved for future use.

The following syntax is simplified from Managed Object Format (MOF) code and is intended to show the definition of the method.

## Syntax

```
SInt32 GetClientsCountByCollections(
     String collectionIDs[],
     UInt32 clientsCount
);
```

#### Parameters

`collectionIDs` Data type: `String` array

Qualifiers: [in]

The specified collection IDs.

`clientsCount` Data type: `UInt32`

Qualifiers: `[out]`

The number of clients in the collections.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).

## See also

[SMS_MigrationCollectionInfo Server WMI Class](sms_migrationcollectioninfo-server-wmi-class.md)
