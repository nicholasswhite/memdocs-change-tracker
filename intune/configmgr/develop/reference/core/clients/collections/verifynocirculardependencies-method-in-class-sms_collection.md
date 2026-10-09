---
description: Learn how to take two collections as arguments and verify that no circular dependencies form using VerifyNoCircularDependencies.
title: "VerifyNoCircularDependencies Method in Class SMS_Collection"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/97159432-14a9-4307-a469-d2f2c75f0e33
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/50565c62-5f6b-4687-be38-323113c72c2e
---

# VerifyNoCircularDependencies Method in Class SMS_Collection

In Configuration Manager, the `VerifyNoCircularDependencies` Windows Management Instrumentation (WMI) class method takes two collections as arguments and verifies that no circular dependencies would be formed if one collection were the parent of another.

The following syntax is simplified from Managed Object Format (MOF) code and is intended to show the definition of the method.

## Syntax

```
sint32 VerifyNoCircularDependencies(
        SMS_Collection ref parentCollection,
        SMS_Collection ref subCollection,
        boolean Result);

```

#### Parameters

`parentCollection` Data type: `ref:SMS_Collection`

Qualifiers: [in]

Reference to an [SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) object path for the parent collection.

`subCollection` Data type: `ref:SMS_Collection`

Qualifiers: [in]

Reference to an [SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) object path for the child collection.

`Result` Data type: `Boolean`

Qualifiers: [out]

true if there are no circular dependencies, false if there are circular dependencies.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) [SMS_Site Server WMI Class](../../servers/configure/sms_site-server-wmi-class.md)
