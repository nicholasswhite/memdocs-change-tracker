---
title: "SMS_ClientDeploymentCollectionBucket Server WMI Class"
description: The SMS_ClientDeploymentCollectionBucket Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that represents a client deployment collection bucket.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ClientDeploymentCollectionBucket Server WMI Class

The `SMS_ClientDeploymentCollectionBucket` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a client deployment collection bucket that is used to display the localized name in the client deployment detail view.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientDeploymentCollectionBucket: SMS_BaseClass
{
    UInt32 BaselineType;
    String Bucket;
    String CollectionID;
    String CollectionName;
    UInt32 FeatureType;
};

```

## Methods

The `SMS_ClientDeploymentCollectionBucket` class does not define any methods.

## Properties

`BaselineType` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The baseline type. Possible values are:

| Value | Baseline type |
| --- | --- |
| 1 | Product Baseline |
| 2 | Staging Baseline |

`Bucket` Data type: `String`

Access type: Read

Qualifiers: [key]

The client deployment status bucket. Possible values are:

| Value |
| --- |
| CDUnknown |
| CDFullCompliant |
| CDInProgress |
| CDNotCompliant |
| CDCriticalError |

`CollectionID` Data type: `String`

Access type: Read

Qualifiers: [key]

The ID of the collection.

`CollectionName` Data type: `String`

Access type: Read

Qualifiers: none

The name of the collection.

`FeatureType` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The feature type. Possible values are:

| Value | Feature type |
| --- | --- |
| 3 | Client Deployment |

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
