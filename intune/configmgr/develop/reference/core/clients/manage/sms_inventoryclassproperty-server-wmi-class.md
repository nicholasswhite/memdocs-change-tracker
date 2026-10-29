---
description: Learn how to use the SMS_InventoryClassProperty Windows Management Instrumentation (WMI) class that is embedded in the SMS_InventoryClass.
title: "SMS_InventoryClassProperty Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_InventoryClassProperty Server WMI Class

The `SMS_InventoryClassProperty` Windows Management Instrumentation (WMI) class is an SMS Provider server class, embedded in the `SMS_InventoryClass` that represents the properties associated with an inventory class in Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_InventoryClassProperty :
{
    UInt32 IsKey;
    String PropertyName;
    String SMSDeviceUri;
    UInt32 Type;
    String Units;
};
```

## Methods

The `SMS_InventoryClassProperty` class does not define any methods.

## Properties

`IsKey` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [not_null]

`true`, if this property is the key of the class. The default value is `false`.

`PropertyName` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

The name of the property. The default value is an empty string.

`SMSDeviceUri` Data type: `String`

Access type: Read/Write

Qualifiers: none

SMS device URI in XML format. This can support multiple device URIs.

`Type` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [not_null]

CIMv2 type of property.

`Units` Data type: `String`

Access type: Read/Write

Qualifiers: [not_null]

The units of the property.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
