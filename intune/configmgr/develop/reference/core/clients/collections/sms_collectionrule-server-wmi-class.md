---
description: Learn how to represent a collection rule using SMS_CollectionRule class in Configuration Manager.
title: "SMS_CollectionRule Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
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

# SMS_CollectionRule Server WMI Class

The `SMS_CollectionRule` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a collection rule in a collection and serves as an abstract base class for [SMS_CollectionRuleDirect Server WMI Class](sms_collectionruledirect-server-wmi-class.md) and [SMS_CollectionRuleQuery Server WMI Class](sms_collectionrulequery-server-wmi-class.md).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CollectionRule
{
      String RuleName;
};
```

## Methods

The `SMS_CollectionRule` class does not define any methods.

## Properties

`RuleName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Descriptive name that identifies the rule. The default value is "".

## Remarks

Class qualifiers for this class include:

- Abstract
- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
