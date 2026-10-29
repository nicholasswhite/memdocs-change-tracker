---
description: Learn how to represent a high performance version of SMS StatMsgAttributes Server class with SMS_StatAttr.
title: "SMS_StatAttr Server WMI Class"
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

# SMS_StatAttr Server WMI Class

The `SMS_StatAttr` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a high-performance version of [SMS_StatMsgAttributes Server WMI Class](sms_statmsgattributes-server-wmi-class.md).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_StatAttr : SMS_BaseClass
{
      UInt32 AttributeID;
      DateTime AttributeTime;
      String AttributeValue;
      SInt64 RecordID;
};
```

## Methods

The `SMS_StatAttr` class does not define any methods.

## Properties

`AttributeID` Data type: `UInt32`

Access type: Read

Qualifiers:

[key]

ID of the type of attribute that is defined by the `AttributeValue` property. See the `AttributeID` property of [SMS_StatMsgAttributes Server WMI Class](sms_statmsgattributes-server-wmi-class.md).

`AttributeTime` Data type: `DateTime`

Access type: Read

Qualifiers: [none]

Date and time, in Universal Coordinated Time (UTC), when the message was generated.

`AttributeValue` Data type: `String`

Access type: Read

Qualifiers: [none]

Attribute value that is determined by the type indicated by the `AttributeID` property.

`RecordID` Data type: `SInt64`

Access type: Read

Qualifiers: none

Record ID of the status message with which the attribute is associated.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  Use this class to associate specific information with a message. The attribute data is not displayed in the message text. Typically, the attribute values are used to query for status messages that reference a particular object. For example, your application can query for the attribute that retrieves all the messages associated with a particular Configuration Manager package.

  Each attribute is stored as an instance of this class. Your application can use the raise status message methods to add attribute values. To delete attribute values, the application deletes the associated status message.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StatMsgAttributes Server WMI Class](sms_statmsgattributes-server-wmi-class.md)
