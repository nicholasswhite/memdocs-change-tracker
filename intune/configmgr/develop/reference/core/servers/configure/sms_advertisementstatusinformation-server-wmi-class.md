---
description: Learn how to represent the state and description for a software distribution or software update status message in Configuration Manager.
title: "SMS_AdvertisementStatusInformation Server WMI Class"
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

# SMS_AdvertisementStatusInformation Server WMI Class

The `SMS_AdvertisementStatusInformation` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the state and description for a software distribution or software update status message.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AdvertisementStatusInformation : SMS_BaseClass
{
      UInt32 MessageID;
      String MessageName;
      UInt32 MessageState;
      String MessageStateName;
};
```

## Methods

The `SMS_AdvertisementStatusInformation` class does not define any methods.

## Properties

`MessageID` Data type: `UInt32`

Access type: Read/write

Qualifiers: [key]

Software distribution or software update message ID.

`MessageName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Short description of the status message.

`MessageState` Data type: `UInt32`

Access type: Read/write

Qualifiers: None

Numeric category (software update states &gt;= 100, software distribution &lt; 100). For more information, see the Remarks section later in this topic.

`MessageStateName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Short description of the message state.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  The `MessageState` property can have one of the following values:

| MessageState | Type | MessageStateName |
| --- | --- | --- |
| -1 | Delivery | Accepted - No further status |
| 0 | Acceptance/Delivery | No Status |
| 1 | Acceptance | Accepted |
| 2 | Acceptance | Rejected |
| 3 | Acceptance | Expired |
| 4 | Delivery | Will Not Rerun |
| 5 | Delivery | Download in Progress |
| 6 | Delivery | Download Complete |
| 7 | Delivery | Canceled |
| 8 | Delivery | Waiting |
| 9 | Delivery | Running |
| 10 | Delivery | Retrying |
| 11 | Delivery | Failed |
| 12 | Delivery | Reboot Pending |
| 13 | Delivery | Succeeded |

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Advertisement Server WMI Class](sms_advertisement-server-wmi-class.md)
