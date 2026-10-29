---
title: "SMS_AdminUIContent Server WMI Class"
description: Learn how to use the SMS_AdminUIContent class although it has no defined methods.
ms.date: "2017-02-15T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
descriptions: Learn about the simplified syntax, methods, properties, and requirements of the SMS_AdminUIContent server class.
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_AdminUIContent Server WMI Class

For internal use only.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AdminUIContent : SMS_BaseClass
{
    DateTime CreationDate;
    String Data;
    String Name;
};

```

## Methods

The `SMS_AdminUIContent` class does not define any methods.

## Properties

`CreationDate` Data type: `DateTime`

Access type: Read-only

Qualifiers: None

Reserved for internal use.

`Data` Data type: `String`

Access type: Read-only

Qualifiers: None

Reserved for internal use.

`Name` Data type: `String`

Access type: Read-only

Qualifiers: [unique, not_null, key]

Reserved for internal use.

## Remarks

Class qualifiers for this class include:

- Read
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
