---
title: "SMS_Client_Reg_MultiString_List Server WMI Class"
description: An SMS Provider server class that represents a list of client registry multi-string items from the site control file.
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

# SMS_Client_Reg_MultiString_List Server WMI Class

The `SMS_Client_Reg_MultiString_List` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that represents a list of client registry multi-string items from the site control file.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Client_Reg_MultiString_List
{
     String ItemType;
     String ValueName;
     String KeyPath;
     String ValueStrings[];
};
```

## Methods

The `SMS_Client_Reg_MultiString_List` class doesn't define any methods.

## Properties

`ItemType` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

Client registry multstring item type.

`ValueName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Property name reflected in the system registry key where the multi-string items are stored. The default value is "".

`KeyPath` Data type: `String`

Access type: Read/Write

Qualifiers: None

Path to the multi-string item. The default value is "".

> [!NOTE]
>
> Do not set this property when updating the `ValueName` property.

`ValueStrings` Data type: `String` Array

Access type: Read/Write

Qualifiers: None

List of strings that serve as registry data values. The meaning of the strings is determined by the `ValueName` property.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  This class behaves the same as [SMS_EmbeddedPropertyList Server WMI Class](sms_embeddedpropertylist-server-wmi-class.md). It's used to represent data that is stored in the system registry with the `REG_MULTI_SZ` data type.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_EmbeddedPropertyList Server WMI Class](sms_embeddedpropertylist-server-wmi-class.md)
