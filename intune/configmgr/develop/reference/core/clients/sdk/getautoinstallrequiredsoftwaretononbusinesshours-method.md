---
description: Learn how to use the GetAutoInstallRequiredSoftwaretoNonBusinessHours method to get the value for AutomaticallyInstallSoftware.
title: "GetAutoInstallRequiredSoftwaretoNonBusinessHours Method in Class CCM_ClientUXSettings"
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

# GetAutoInstallRequiredSoftwaretoNonBusinessHours Method in Class CCM_ClientUXSettings

The `GetAutoInstallRequiredSoftwaretoNonBusinessHours` Windows Management Instrumentation (WMI) class method in Configuration Manager that gets the value for `AutomaticallyInstallSoftware`.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetAutoInstallRequiredSoftwaretoNonBusinessHours
{
    [OUT]   Boolean AutomaticallyInstallSoftware
};
```

## Parameters

`AutomaticallyInstallSoftware` Data type: `Boolean`

Qualifiers: [id("0"), out]

`true` if necessary software should be automatically installed during nonbusiness hours.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
