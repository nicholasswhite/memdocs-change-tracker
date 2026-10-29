---
description: Learn how to use SMS_SoftwareConversionRules to describe rules to convert the company or product name resource string into a standard name.
title: "SMS_SoftwareConversionRules Server WMI Class"
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

# SMS_SoftwareConversionRules Server WMI Class

The `SMS_SoftwareConversionRules` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that describes the rules to convert the company or product name resource string into a standard name for software inventory. For example, different Microsoft products might contain variations of the Microsoft company name, for example, "Microsoft Corporation" or "Microsoft."

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SoftwareConversionRules : SMS_BaseClass
{
     String ConvertType;
     String NewName;
     String OriginalName;
     UInt32 RuleId;
};
```

## Methods

The `SMS_SoftwareConversionRules` class doesn't define any methods.

## Properties

`ConvertType` Data type: **String**

Access type: Read/Write

Type of resource string to convert. Possible values are:

- Manufacturer (default)
- Product

  `NewName` Data type: **String**

  Access type: Read/Write

  Qualifiers: [Not_Null]

  Name reported to software inventory. The default value is "".

  `OriginalName` Data type: **String**

  Access type: Read/Write

  Qualifiers: [Not_Null]

  Original company or product name. The default value is "".

  The original name can contain SQL wildcard characters (&amp;, _, [], and [^]), but the `OriginalName` and `ConvertType`combination must be unique.

  `RuleId` Data type: **UInt32**

  Access type: Read-only

  Qualifiers: [key, read, Not_Null]

  Unique ID of the rule. The default value is 0.

## Remarks

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
