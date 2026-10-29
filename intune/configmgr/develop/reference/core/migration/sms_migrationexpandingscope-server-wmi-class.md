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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
