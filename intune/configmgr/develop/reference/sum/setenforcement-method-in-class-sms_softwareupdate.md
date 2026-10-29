---
title: "SetEnforcement Method in Class SMS_SoftwareUpdate"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn how to set policy enforcement rules for software updates by editing the 'SetEnforcement' class method in the Configuration Manager.
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SetEnforcement Method in Class SMS_SoftwareUpdate

The `SetEnforcement` Windows Management Instrumentation (WMI) class method, in Configuration Manager, sets policy enforcement for the software update.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 SetEnforcement(
     Boolean Enforced,
     DateTime EffectiveDate
);
```

#### Parameters

`Enforced` Data type: `Boolean`

Qualifiers: [in]

`true` if policy enforcement is enabled for the configuration item.

`EffectiveDate` Data type: `DateTime`

Qualifiers: [in]

The date and time, in Coordinated Universal Time (UTC), when the configuration item is compliant.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdate Server WMI Class](sms_softwareupdate-server-wmi-class.md)
