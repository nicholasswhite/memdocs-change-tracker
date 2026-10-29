---
title: "CreateRelationship method in class SMS_UserMachineRelationship"
description: Use this WMI class method to add a user device affinity.
ms.date: "2020-08-26T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
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

# CreateRelationship method in class SMS_UserMachineRelationship

The `CreateRelationship` WMI class method creates a relationship between a user and a device.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 CreateRelationship (
     uint32 MachineResourceId,
     string UserAccountName,
     uint32 SourceId,
     uint32 TypeId
);
```

## Parameters

`MachineResourceId` Data type: `UInt32`

Qualifiers: `[in]`

Unique Configuration Manager-supplied identifier for the resource.

`UserAccountName` Data type: `String`

Qualifiers: `[in]`

User account name. For example, `contoso\jqpublic`.

`SourceId` Data type: `UInt32`

Qualifiers: `[in]`

Source object identifier for dependency.

| Value | Name | Description |
| --- | --- | --- |
| `1` | Self-service portal | The end user enabled the relationship by selecting the option in Software Center. |
| `2` | Administrator | An administrator created the relationship manually in the console. |
| `3` | User | Unused/deprecated. |
| `4` | Usage agent | The threshold of activity triggered a relationship to be created. |
| `5` | Device management | The user and device were tied together during on-prem MDM enrollment. |
| `6` | OSD | The user and device were tied together as part of an OS deployment task sequence. |
| `7` | Fast install | The user/device were tied together temporarily to enable an on-demand install from the catalog if no UDA relationship installed before the Install was triggered. |
| `8` | Exchange Server connector | The device was provisioned through Exchange ActiveSync. |

`TypeId` Data type: `UInt32`

Qualifiers: `[in, optional]`

An array of types for this relationship. For a value of `1`, the **UniqueUserName** is the primary user. If the value is null, they aren't the primary user.

## Return values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime requirements

For more information, see [Configuration Manager server runtime requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development requirements

For more information, see [Configuration Manager server development requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_Application server WMI class](../../../apps/sms_application-server-wmi-class.md)
