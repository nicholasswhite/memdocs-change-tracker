---
title: "SMS_MigrationExpandingScope Server WMI Class"
description: The SMS_MigrationExpandingScope class represents collections that have the expanding scope problem when migrated to System Center 2012 Configuration Manager.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SMS_MigrationExpandingScope Server WMI Class

The `SMS_MigrationExpandingScope` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the collections that have the problem of expanding scope when migrated to System Center 2012 Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MigrationExpandingScope : SMS_BaseClass
{
    UInt32 CollectionEntityID;
    String CollectionEntityName;
    String CollectionWMIObjectPath;
    UInt32 TargetingEntityID;
    String TargetingEntityName;
    String TargetingWMIObjectPath;
};
```

## Methods

The `SMS_MigrationExpandingScope` class does not define any methods.

## Properties

`CollectionEntityID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

Unique identifier for the collection.

`CollectionEntityName` Data type: `String`

Access type: Read-only

Qualifiers: none

The collection entity display name.

`CollectionWMIObjectPath` Data type: `String`

Access type: Read-only

Qualifiers: none

The collection entity WMI path.

`TargetingEntityID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

Unique identifier for the targeting entity.

`TargetingEntityName` Data type: `String`

Access type: Read-only

Qualifiers: none

The targeting entity display name.

`TargetingWMIObjectPath` Data type: `String`

Access type: Read-only

Qualifiers: none

The targeting entity WMI path.

## Remarks

When you create a migration job, consider whether to specify a new limit to the collection to restrict the scope for each of such collections.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).
