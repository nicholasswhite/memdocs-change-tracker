---
description: Article describing how to use FindResourceSite in Configuration Manager to get site code information for resources from SQL.
title: "FindResourceSite Method in Class SMS_Query"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# FindResourceSite Method in Class SMS_Query

The `FindResourceSite` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets site code information for resources from SQL.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 FindResourceSite(
   Boolean IncludeSubCollections,
   String SiteCode[],
   UInt32 ResourceNumber[]
);
```

#### Parameters

`IncludeSubCollections` Data type: `Boolean`

Qualifiers: [in, optional]

`true` if subcollections should be included. The default value is `false`.

`SiteCode` Data type: `String` Array

Qualifiers: [out]

Site code of the Configuration Manager site.

`ResourceNumber` Data type: `UInt32` Array

Qualifiers: [out]

The resource number.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Query Server WMI Class](sms_query-server-wmi-class.md)
