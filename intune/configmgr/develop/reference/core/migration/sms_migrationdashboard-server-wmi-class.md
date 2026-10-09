---
description: Learn how to represent the migration feature dashboard using SMS_MigrationDashboard class in Configuration Manager.
title: "SMS_MigrationDashboard Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SMS_MigrationDashboard Server WMI Class

The `SMS_MigrationDashboard` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the migration feature dashboard.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MigrationDashboard : SMS_BaseClass
{
    DateTime ClientMigrationLastUpdated;
    DateTime JobStatisticsLastUpdated;
    DateTime LastSuccessfulSynced;
    UInt32 NumOfDestinationSites;
    UInt32 NumOfJobCompleted;
    UInt32 NumOfJobFailed;
    UInt32 NumOfJobInProgress;
    UInt32 NumOfSourceSiteClients;
    UInt32 NumOfSourceSiteClientsExcluded;
    UInt32 NumOfSourceSiteClientsMigrated;
    UInt32 NumOfSourceSiteClientsRemaining;
    UInt32 NumOfSourceSiteObjects;
    UInt32 NumOfSourceSiteObjectsExcluded;
    UInt32 NumOfSourceSiteObjectsMigrated;
    UInt32 NumOfSourceSiteObjectsRemaining;
    UInt32 NumOfSourceSites;
    DateTime ObjectMigrationLastUpdated;
    String SourceCentralSiteFQDN;
    String Version;
};
```

## Methods

The `SMS_MigrationDashboard` class does not define any methods.

## Properties

`ClientMigrationLastUpdated` Data type: `DateTime`

Access type: Read-only

Qualifiers: none

The last time the migration monitored client status changed.

`JobStatisticsLastUpdated` Data type: `DateTime`

Access type: Read-only

Qualifiers: none

Last job statistics update time.

`LastSuccessfulSynced` Data type: `DateTime`

Access type: Read-only

Qualifiers: none

Last time that the data gathering process was performed successfully.

`NumOfDestinationSites` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Number of destination sites.

`NumOfJobCompleted` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Number of jobs completed.

`NumOfJobFailed` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Number of jobs failed.

`NumOfJobInProgress` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Number of jobs in progress.

`NumOfSourceSiteClients` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of clients in the source site hierarchy.

`NumOfSourceSiteClientsExcluded` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of clients excluded from the source site hierarchy.

`NumOfSourceSiteClientsMigrated` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of clients migrated from the source site hierarchy.

`NumOfSourceSiteClientsRemaining` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of clients remaining in the source site hierarchy.

`NumOfSourceSiteObjects` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of objects in the source site hierarchy.

`NumOfSourceSiteObjectsExcluded` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of objects excluded from the source site hierarchy.

`NumOfSourceSiteObjectsMigrated` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of objects migrated from the source site hierarchy.

`NumOfSourceSiteObjectsRemaining` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Total number of objects remaining in the source site hierarchy.

`NumOfSourceSites` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Number of source sites.

`ObjectMigrationLastUpdated` Data type: `DateTime`

Access type: Read-only

Qualifiers: none

Last object migration update time.

`SourceCentralSiteFQDN` Data type: `String`

Access type: Read-only

Qualifiers: [key]

Source central site FQDN.

`Version` Data type: `String`

Access type: Read-only

Qualifiers: None

The version of the source site.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

## Remarks

You can use the migration feature dashboard to get the overall status of migration. For example, you can get the current active source hierarchy, how many objects got migrated, the last successful data gathering, and other status information.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).
