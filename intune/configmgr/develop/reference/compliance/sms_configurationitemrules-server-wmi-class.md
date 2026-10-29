---
description: Learn how to represent configuration item rules using SMS_ConfigurationItemRules in Configuration Manager.
title: "SMS_ConfigurationItemRules Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ConfigurationItemRules Server WMI Class

The `SMS_ConfigurationItemRules` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents configuration item rules.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ConfigurationItemRules : SMS_BaseClass
{
    UInt32 CI_ID;
    String CI_UniqueID;
    String ModelName;
    UInt32 Rule_ID;
    String Rule_UniqueID;
    String RuleDescription;
    String RuleName;
};
```

## Methods

The `SMS_ConfigurationItemRules` class does not define any methods.

## Properties

`CI_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`CI_UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`ModelName` Data type: `String`

Access type: Read/Write

Qualifiers: none

[SMS_ConfigurationItemLatestBaseClass Server WMI Class](sms_configurationitemlatestbaseclass-server-wmi-class.md)

`Rule_ID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

The database identifier of a rule defined in a configuration item.

`Rule_UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: none

Uniquely identifies a rule defined in the configuration item and is used for reporting rule level details.

`RuleDescription` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description of the rule.

`RuleName` Data type: `String`

Access type: Read/Write

Qualifiers: none

[SMS_CollectionRule Server WMI Class](../core/clients/collections/sms_collectionrule-server-wmi-class.md)

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
