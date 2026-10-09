---
description: Learn how to retrieve an application deployment type property using GetProperty class in Configuration Manager.
title: "GetProperty Method in Class CCM_AppDeploymentType"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# GetProperty Method in Class CCM_AppDeploymentType

The `GetProperty` Windows Management Instrumentation (WMI) class method in Configuration Manager that retrieves an application deployment type property.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetProperty
{
    [IN]    UInt32 LanguageId
    [IN]    String PropertyName
    [OUT]   String PropertyValue
};
```

## Parameters

`LanguageId` Data type: `UInt32`

Qualifiers: [id("0"), in]

Language identifier.

`PropertyName` Data type: `String`

Qualifiers: [id("1"), in]

Property name.

`PropertyValue` Data type: `String`

Qualifiers: [id("2"), out]

Property value.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
