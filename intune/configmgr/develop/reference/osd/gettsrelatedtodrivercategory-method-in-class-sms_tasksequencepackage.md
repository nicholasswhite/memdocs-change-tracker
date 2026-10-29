---
title: "GetTSRelatedToDriverCategory Method in Class SMS_TaskSequencePackage"
description: The GetTSRelatedToDriverCategory WMI class method gets task sequence packages related to the specified category.
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

# GetTSRelatedToDriverCategory Method in Class SMS_TaskSequencePackage

The `GetTSRelatedToDriverCategory` Windows Management Instrumentation (WMI) class method, in Configuration Manager, that gets task sequence packages related to the specified category.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetTSRelatedToDriverCategory
{
    [IN]    String CategoryUniqueId,
    [OUT]   String PacakgeIds[]
    [OUT]   String PackageNames[]
};
```

## Parameters

`CategoryUniqueId` Data type: `String`

Qualifiers: [id("0"), in]

Unique ID of the category instance. This ID is unique across sites. The string length can be up to 512 characters.

`PacakgeIds` Data type: `String` Array

Qualifiers: [id("2"), out]

Package identifiers for packages related to the specified category.

> [!NOTE]
>
> The incorrect spelling of the variable "PacakgeIds" is hardcoded in WMI.

`PackageNames` Data type: `String` Array

Qualifiers: [id("3"), out]

Package names for packages related to the specified category.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
