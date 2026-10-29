---
title: "SMS_UserMachineRelationship server WMI class"
description: Use this server WMI class to manage user device affinity.
ms.date: "2020-08-26T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_UserMachineRelationship server WMI class

The `SMS_UserMachineRelationship` WMI class contains relationships between a device and its primary users.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_UserMachineRelationship : SMS_BaseClass
{
    DateTime CreationTime;
    Boolean IsActive;
    UInt32 RelationshipResourceID;
    UInt32 ResourceClientType;
    UInt32 ResourceID;
    String ResourceName;
    UInt32 Sources[];
    UInt32 Types[];
    String UniqueUserName;
};
```

## Methods

The `SMS_UserMachineRelationship` class defines the following methods.

| Method | Description |
| --- | --- |
| [AddSource Method in Class SMS_UserMachineRelationship](addsource-method-in-class-sms_usermachinerelationship.md) | Adds a source for the relationship between the user and the device. |
| [AddType Method in Class SMS_UserMachineRelationship](addtype-method-in-class-sms_usermachinerelationship.md) | Adds a type of the relationship between a user and a device. |
| [CreateRelationship Method in Class SMS_UserMachineRelationship](createrelationship-method-in-class-sms_usermachinerelationship.md) | Creates a relationship between a user and a device. |
| [RemoveSource Method in Class SMS_UserMachineRelationship](removesource-method-in-class-sms_usermachinerelationship.md) | Removes a source for the relationship between a user and a device. |
| [RemoveType Method in Class SMS_UserMachineRelationship](removetype-method-in-class-sms_usermachinerelationship.md) | Removes a type of the relationship between a user and a device. |

## Properties

`CreationTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [read]

The time that the relationship was created.

`IsActive` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

**TRUE** if the relationship is active.

`RelationshipResourceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

The unique identifier for this relationship.

`ResourceClientType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Client type for computer.

`ResourceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

The resource ID of the device.

`ResourceName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

The resource name of the device.

`Sources` Data type: `UInt32` Array

Access type: Read-only

Qualifiers: [read]

An array of sources for this relationship, with one of the following values:

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
| `9` | Secure usage agent |  |

`Types` Data type: `UInt32` Array

Access type: Read-only

Qualifiers: [read]

An array of types for this relationship. For a value of `1`, the **UniqueUserName** is the primary user. If the value is null, they aren't the primary user.

`UniqueUserName` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

User name in domain\user format.

## Remarks

## Requirements

### Runtime requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
