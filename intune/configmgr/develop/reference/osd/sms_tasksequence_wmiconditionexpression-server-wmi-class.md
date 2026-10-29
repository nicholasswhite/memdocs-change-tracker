---
title: "SMS_TaskSequence_WMIConditionExpression Server WMI Class"
description: Represents a condition expression to check for the existence of results of a WMI query.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_TaskSequence_WMIConditionExpression Server WMI Class

The `SMS_TaskSequence_WMIConditionExpression` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a condition expression to check for the existence of results of a WMI query.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequence_WMIConditionExpression : SMS_TaskSequence_ConditionExpression
{
      String Namespace;
      String Query;
};
```

## Methods

The `SMS_TaskSequence_WMIConditionExpression` class does not define any methods.

## Properties

`Namespace` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null]

Namespace for the query.

`Query` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_Null, AllowedLen("1-16384")]

The WQL query for the condition expression. The length is between 1 and 16,384 characters.

## Remarks

The query result set is the results that satisfy the condition. For example, if you need to identify if a computer has at least one NTFS partition, you would use the following query:

```
Select * from win32_logicaldisk where FileSystem='NTFS'
```

There are no class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers that are included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
