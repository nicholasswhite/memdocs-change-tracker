---
description: Learn how to use the SMS_TaskSequence_FileConditionExpression class to represent a condition expression to check for the existence of a file and its creation time.
title: "SMS_TaskSequence_FileConditionExpression Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_TaskSequence_FileConditionExpression Server WMI Class

The `SMS_TaskSequence_FileConditionExpression` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a condition expression to check for the existence of a file and its creation time.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_FileConditionExpression : SMS_TaskSequence_ConditionExpression
{
      DateTime DateTime;
      String DateTimeOperator;
      String Path;
      String Version;
      String VersionOperator;
};
```

## Methods

The `SMS_TaskSequence_FileConditionExpression` class does not define any methods.

## Properties

`DateTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

The date and time used to evaluate the target computer for a specific, user-specified timestamp on a file.

The timestamp that is displayed in the Configuration Manager console is the local time on the computer running the Configuration Manager console. The timestamp is converted to Coordinated Universal Time (UTC). The comparison on the target computer uses the UTC timestamp so that time zones and daylight savings time do not affect the comparison.

`DateTimeOperator` Data type: `String`

Access type: Read/Write

Qualifiers: None

The date and time operator. Possible values are:

- equals
- notEquals
- less
- lessEqual
- greater
- greaterEqual

  `Path` Data type: `String`

  Access type: Read/Write

  Qualifiers: [Not_Null]

  The path on the target computer for the file that is being verified. The path can contain embedded task sequence and system environment variables, for example, %*windir*%\notepad.exe.

  `Version` Data type: `String`

  Access type: Read/Write

  Qualifiers: None

  Value used to evaluate the target computer for a specific, user-specified version of a file.

  `VersionOperator` Data type: `String`

  Access type: Read/Write

  Qualifiers: None

  The version operator. Possible values are:
- equals
- notEquals
- less
- lessEqual
- greater
- greaterEqual

## Remarks

There are no class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
