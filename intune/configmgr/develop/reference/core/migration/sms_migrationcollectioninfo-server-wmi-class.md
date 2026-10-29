---
title: "SMS_MigrationCollectionInfo Server WMI Class"
description: The SMS_MigrationCollectionInfo WMI class is an SMS Provider server class that represents the collections created on the current active 2007 hierarchy.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_MigrationCollectionInfo Server WMI Class

The `SMS_MigrationCollectionInfo` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the collections created on the current active Configuration Manager 2007 hierarchy.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MigrationCollectionInfo : SMS_BaseClass
{
    UInt32 ChildCount;
    String Children;
    UInt32 CollectionEntityID;
    String CollectionName;
    UInt32 CollectionType;
    UInt32 Count;
    Boolean IsTop;
    UInt32 LimitToCount;
    String LimitTos;
    UInt32 SiteCodeCount;
    String SiteCodes;
    String SourceSiteCollectionID;
    UInt32 SourceSiteID;
    UInt32 Status;
};
```

## Methods

The following table lists the methods in the `SMS_MigrationCollectionInfo` class.

| Method | Description |
| --- | --- |
| [GetClientsCountByCollections Method in Class SMS_MigrationCollectionInfo](getclientscountbycollections-method-in-class-sms_migrationcollectioninfo.md) | Retrieves the number of clients in the specified collection. **Warning:** This method is reserved for future use. |

## Properties

`ChildCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

The count of child collections.

`Children` Data type: `String`

Access type: Read-only

Qualifiers: none

The child collection Ids, separated by ','.

`CollectionEntityID` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Entity ID of this collection.

`CollectionName` Data type: `String`

Access type: Read-only

Qualifiers: none

Display name of the collection.

`CollectionType` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

The type of the collection.

| Value | Collection type |
| --- | --- |
| 0 | Mixed |
| 1 | User |
| 2 | Device |
| 3 | UnknownArchitecture |
| 4 | UnknownQuery |
| 5 | Folder |

`Count` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

The total number of devices or users in this collection.

`IsTop` Data type: `Boolean`

Access type: Read-only

Qualifiers: none

`true` if the collection is a top collection which linked to the root.

`LimitToCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

The total number of collections that the collection is limited to.

`LimitTos` Data type: `String`

Access type: Read-only

Qualifiers: none

The string that concatenate all ID of collections that the collection is limit to, separated by ','.

`SiteCodeCount` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

The count of site codes embedded in the query.

`SiteCodes` Data type: `String`

Access type: Read-only

Qualifiers: none

The string that concatenate all site codes that embedded in the collection query string, separated by ','.

`SourceSiteCollectionID` Data type: `String`

Access type: Read-only

Qualifiers: [key]

Unique identifier for the collection in the source site.

`SourceSiteID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key]

Unique identifier for the source site in `SMS_MigrationSourceSite`.

`Status` Data type: `UInt32`

Access type: Read-only

Qualifiers: none

Status of the collection.

## Remarks

Each instance of this class represents a collection.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).
