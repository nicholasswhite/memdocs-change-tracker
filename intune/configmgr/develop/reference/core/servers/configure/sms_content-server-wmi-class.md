---
title: "SMS_Content Server WMI Class"
description: Learn how the SMS_Content class is an SMS Provider server class, in Configuration Manager, that provides additional information about a CI_Content instance.
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

# SMS_Content Server WMI Class

The `SMS_Content` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides additional information about a `CI_Content` instance.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Content : SMS_BaseClass
{
    String ContentDescription;
    UInt32 ContentFlags;
    String ContentHash;
    UInt32 ContentHashVersion;
    SInt32 ContentID;
    String ContentSource;
    UInt32 ContentType;
    String ContentUniqueID;
    UInt32 ContentVersion;
    UInt32 ObjectTypeID;
    String RelatedContentID;
    String SecurityKey;
};
```

## Methods

The following table lists the methods in the `SMS_Content` class.

| Method | Description |
| --- | --- |
| [IsOfficeContent Method in Class SMS_Content](isofficecontent-method-in-class-sms_content.md) | Specifies whether content is Microsoft Office content. |

## Properties

`ContentDescription` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description of the content.

`ContentFlags` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

This specifies additional attributes for content instance.

| Value | Content flag |
| --- | --- |
| 8 | DOWNLOAD_ON_DEMAND_FROM_LOCAL_DP |
| 12 | DOWNLOAD_FROM_LOCAL_DISPPOINT |
| 13 | DOWNLOAD_LOCAL_PARTIALDOWNLOADTOLOCAL |
| 14 | DOWNLOAD_FROM_REMOTE_DISPPOINT |
| 15 | DOWNLOAD_REMOTE_PARTIALDOWNLOADTOLOCAL |
| 16 | DOWNLOAD_ENABLE_PEER_CACHING |
| 17 | DP_NO_FALLBACK_UNPROTECTED |
| 24 | DO_NOT_DOWNLOAD |
| 25 | PERSIST_IN_CACHE |

`ContentHash` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Hash of the content.

`ContentHashVersion` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

This specifies the hash version used to calculate the content hash.

`ContentID` Data type: `SInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifier for the content.

`ContentSource` Data type: `String`

Access type: Read/Write

Qualifiers: none

This specifies the source location where content files are stored.

`ContentType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Type of the content.

`ContentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Unique identifier for the content.

`ContentVersion` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Version of the content.

`ObjectTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

The security type of the content.

`RelatedContentID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Specifies the related content associated with this content.

`SecurityKey` Data type: `String`

Access type: Read/Write

Qualifiers: none

The security key of the content. Content may be secured by application or package.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
