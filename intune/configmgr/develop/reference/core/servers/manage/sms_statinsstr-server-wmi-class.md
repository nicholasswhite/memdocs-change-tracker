---
description: Learn how to use the SMS_StatInsStr Class to represent a high-performance version of SMS_StatMsgInsStrings Server WMI class.
title: "SMS_StatInsStr Server WMI Class"
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

# SMS_StatInsStr Server WMI Class

The `SMS_StatInsStr` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a high-performance version of [SMS_StatMsgInsStrings Server WMI Class](sms_statmsginsstrings-server-wmi-class.md).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_StatInsStr : SMS_BaseClass
{
      UInt32 InsStrIndex;
      String InsStrValue;
      SInt64 RecordID;
};
```

## Methods

The `SMS_StatInsStr` class does not define any methods.

## Properties

`InsStrIndex` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The index defining the order of the insertion strings. The index directly relates to the insertion points in the status message.

`InsStrValue` Data type: `String`

Access type: Read

Qualifiers: none

Text to insert into the insertion point.

`RecordID` Data type: `SInt64`

Access type: Read

Qualifiers: none

Record ID of the status message to which the insertion point belongs.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  This class represents insertion strings for Configuration Manager component messages and user-defined messages. The status message is represented by [SMS_StatusMessage Server WMI Class](sms_statusmessage-server-wmi-class.md). Your application can use the [RaiseRawStatusMsg Method in Class SMS_StatusMessage](raiserawstatusmsg-method-in-class-sms_statusmessage.md) to add insertion strings. To delete insertion strings, the application deletes the associated status message.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StatMsgInsStrings Server WMI Class](sms_statmsginsstrings-server-wmi-class.md) [SMS_StatusMessage Server WMI Class](sms_statusmessage-server-wmi-class.md)
