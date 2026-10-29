---
description: Learn how to use SMS_EndpointProtectionDashboardBucket Windows Management Instrumentation (WMI) class in Configuration Manager.
title: "SMS_EndpointProtectionDashboardBucket Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_EndpointProtectionDashboardBucket Server WMI Class

The `SMS_EndpointProtectionDashboardBucket` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_EndpointProtectionDashboardBucket : SMS_BaseClass
{
    String Bucket;
    String CollectionID;
    String CollectionName;
};
```

## Methods

The `SMS_EndpointProtectionDashboardBucket` class does not define any methods.

## Properties

`Bucket` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Dashboard bucket summarized.

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Identifier of the collection summarized.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the collection summarized.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
