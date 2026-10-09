---
title: "SMS_ApplicationCondition Server WMI Class"
description: An SMS Provider server class that represents relationships between global conditions and applications.
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

# SMS_ApplicationCondition Server WMI Class

The `SMS_ApplicationCondition` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents relationships between global conditions and applications.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ApplicationCondition : SMS_BaseClass
{
    String ApplicationGUID;
    String ConditionDisplayName;
    UInt32 ConditionID;
    String ConditionModelName;
};
```

## Methods

The `SMS_ApplicationCondition` class does not define any methods.

## Properties

`ApplicationGUID` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Unique identifier of the application.

`ConditionDisplayName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Condition display name.

`ConditionID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Identifier of the application condition.

`ConditionModelName` Data type: `String`

Access type: Read-only

Qualifiers: [not_null, read]

Model name of the condition.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
