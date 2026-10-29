---
title: "SMS_DeploymentInfoFlat Server WMI Class"
description: Learn how the SMS_DeploymentInfoFlat Windows Management Instrumentation (WMI) class is an SMS Provider server class.
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

# SMS_DeploymentInfoFlat Server WMI Class

The `SMS_DeploymentInfoFlat` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents all kinds of flattened deployment relations (includes dependence and supersedence).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DeploymentInfoFlat : SMS_BaseClass
{
    String CollectionID;
    String CollectionName;
    String DeploymentID;
    String DeploymentName;
    UInt32 DeploymentTypeID;
    String TargetName;
    UInt32 TargetSecurityTypeID;
    String TargetSubName;
};
```

## Methods

The `SMS_DeploymentInfoFlat` class doesn't define any methods.

## Properties

`CollectionID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Existing collection to which the advertisement is targeted.

`CollectionName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name of the collection to which the advertisement is advertising.

`DeploymentID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Unique auto-generated key.

`DeploymentName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Plain text name of the deployment (advertisement/assignment).

`DeploymentTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [enumeration, key]

Deployment type identifier.

`TargetName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Package name, if the target is a package. Application name, if it's an application. Update name, if it's an update.

`TargetSecurityTypeID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Security type identifier of the object type. For example, if the object is a package, its `2`.

`TargetSubName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Program name if it's a package, otherwise leave this value empty.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
