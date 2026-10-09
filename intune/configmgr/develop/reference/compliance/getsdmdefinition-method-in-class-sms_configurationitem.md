---
description: Learn how to retrieve the System Definition Model (SDM) definition of the configuration item in XML format using GetSDMDefinition class method.
title: "GetSDMDefinition Method in Class SMS_ConfigurationItem"
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

# GetSDMDefinition Method in Class SMS_ConfigurationItem

The `GetSDMDefinition` Windows Management Instrumentation (WMI) class method, in Configuration Manager, retrieves the System Definition Model (SDM) definition of the configuration item in XML format.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetSDMDefinition(
     String SDMDefinition
);
```

#### Parameters

`SDMDefinition` Data type: `String`

Qualifiers: [out]

The SDM definition in XML format.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

For more information about SDM definitions, see About Authoring Configuration Baselines and Configuration Items.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ConfigurationItem Server WMI Class](sms_configurationitem-server-wmi-class.md)
