---
description: Learn how to reload the install map from the database, which repopulates the classes using Refresh class method.
title: "Refresh Method in Class SMS_SiteInstallMap"
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

# Refresh Method in Class SMS_SiteInstallMap

The `Refresh` Windows Management Instrumentation (WMI) class method, in Configuration Manager, reloads the install map from the database, which repopulates the classes.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 Refresh( );
```

#### Parameters

None.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Remarks

This method is used in the rare case when a new component is added by Configuration Manager site setup and the SMS Provider is located on a remote SQL Server computer that might not be restarted. Generally it isn't necessary for your application to call this method because the SMS Provider copy of the install map will be up to date.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SiteInstallMap Server WMI Class](sms_siteinstallmap-server-wmi-class.md)
