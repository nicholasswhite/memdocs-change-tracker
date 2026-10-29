---
title: "SMS_TaskSequencePackageReference_All Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn about the simplified syntax, methods, properties, and requirements of the SMS_TaskSequencePackageReference_All server class.
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

# SMS_TaskSequencePackageReference_All Server WMI Class

The `SMS_TaskSequencePackageReference_All` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that allows the retrieval of all task sequence package or application references (including those that do not contain any content files).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequencePackageReference_All : SMS_BaseClass
{
    String ObjectID;
    String PackageID;
    String RefPackageID;
};
```

## Methods

The `SMS_TaskSequencePackageReference_All` class does not define any methods.

## Properties

`ObjectID` Data type: `String`

Access type: Read

Qualifiers: [key]

If the Task Sequence reference is to a legacy package, this property is the package identifier of the legacy package. If the Task Sequence reference is to an application, this property is the package identifier of the application.

`PackageID` Data type: `String`

Access type: Read

Qualifiers: [key]

Package identifier of the task sequence for which the user requests package or application references.

`RefPackageID` Data type: `String`

Access type: Read

Qualifiers: none

If the Task Sequence reference is to a legacy package, this property is the package identifier of the legacy package. If the Task Sequence reference is to an application, this property is the package identifier of the application.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
