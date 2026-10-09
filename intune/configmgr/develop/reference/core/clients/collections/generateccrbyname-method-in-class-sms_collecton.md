---
description: Learn how to generate a client configuration request by computer name using the GenerateCCRByName class method.
title: "GenerateCCRByName Method in Class SMS_Collecton"
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

# GenerateCCRByName Method in Class SMS_Collecton

The `GenerateCCRByName` Windows Management Instrumentation (WMI) class method generates a client configuration request by computer name.

The following syntax is simplified from Managed Object Format (MOF) code and is intended to show the definition of the method.

## Syntax

```
SInt32 GenerateCCRByName(
     String Name
     String PushSiteCode
     Boolean Forced
);
```

#### Parameters

`Name` Data type: `String`

Qualifiers: [in]

Name of the computer.

`PushSiteCode` Data type: `String`

Qualifiers: [in]

PushSiteCode defines which site will initiate the actual push. The specified site will push its client files to the client and do the actual installation.

`Forced` Data type: `Boolean`

Qualifiers: [in]

`true` to force installation. The value defaults to false, if not specified.

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
