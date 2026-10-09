---
title: "SMS_TaskSequenceAppReferenceDps Server WMI Class"
description: An SMS Provider server class that represents a distribution point to which a Configuration Manager application in the task sequence is distributed.
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

# SMS_TaskSequenceAppReferenceDps Server WMI Class

The `SMS_TaskSequenceAppReferenceDps` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a distribution point to which a Configuration Manager application in the task sequence is distributed.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequenceAppReferenceDps :
{
    String Hash;
    String PackageID;
    String ServerNALPath;
    String SiteCode;
    UInt32 SourceVersion;
    String TaskSequenceID;
};
```

## Methods

The `SMS_TaskSequenceAppReferenceDps` class does not define any methods.

## Properties

`Hash` Data type: `String`

Access type: Read/Write

Qualifiers: none

Hash for application.

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Package ID for application.

`ServerNALPath` Data type: `String`

Access type: Read/Write

Qualifiers: none

NALPath for distribution point.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: none

Site code for distribution point.

`SourceVersion` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Source version for application.

`TaskSequenceID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID for task sequence package.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
