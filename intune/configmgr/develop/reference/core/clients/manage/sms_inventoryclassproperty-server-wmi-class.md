---
description: Learn how to use the SMS_InventoryClassProperty Windows Management Instrumentation (WMI) class that is embedded in the SMS_InventoryClass.
title: "SMS_InventoryClassProperty Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
