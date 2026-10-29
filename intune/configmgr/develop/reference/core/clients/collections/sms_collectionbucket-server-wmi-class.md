---
description: Learn how to represent the joining of collection and bucket with the SMS_CollectionBucket class.
title: "SMS_CollectionBucket Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CollectionBucket Server WMI Class

The `SMS_CollectionBucket` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents joining of collection and bucket. By default, all collections will have a client health related bucket, while the endpoint protection bucket is only applicable to endpoint protection allowed collections.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CollectionBucket : SMS_BaseClass
{
    String Bucket;
    String CollectionID;
    String CollectionName;
    UInt32 FeatureType;
};
```

## Methods

The `SMS_CollectionBucket` class does not define any methods.

## Properties

`Bucket` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Bucket summarized.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier of collection summarized.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of collection summarized.

`FeatureType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Identifier of feature type.

| Value | Feature Type |
| --- | --- |
| 1 | EndPoint Protection |
| 2 | Client Check |

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
