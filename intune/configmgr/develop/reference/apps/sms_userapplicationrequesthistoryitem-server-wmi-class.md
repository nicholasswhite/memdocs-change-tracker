---
description: Learn how to represent an update to an instance of SMS_UserApplicationRequest using SMS_UserApplicationRequestHistoryItem class.
title: "SMS_UserApplicationRequestHistoryItem Server WMI Class"
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

# SMS_UserApplicationRequestHistoryItem Server WMI Class

The `SMS_UserApplicationRequestHistoryItem` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents an update to an instance of `SMS_UserApplicationRequest`.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_UserApplicationRequestHistoryItem :
{
    String Comments;
    String ModifiedBy;
    DateTime ModifiedDate;
    UInt32 State;
};
```

## Methods

The `SMS_UserApplicationRequestHistoryItem` class does not define any methods.

## Properties

`Comments` Data type: `String`

Access type: Read/Write

Qualifiers: none

Comments entered to explain why the change occurred. These could be user's comment explaining why they are requesting the application or approver comments explaining why the application was approved or denied.

`ModifiedBy` Data type: `String`

Access type: Read/Write

Qualifiers: none

The user who made the change to the request.

`ModifiedDate` Data type: `DateTime`

Access type: Read/Write

Qualifiers: none

The date when the change to the request was made.

`State` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

The state of the request after the change was made. Possible values are:

| Value | State |
| --- | --- |
| 1 | Requested |
| 2 | Canceled |
| 3 | Denied |
| 4 | Approved |

## Remarks

## Requirements

Each time a request is updated, an instance of this class is created to track the history of the request.

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_UserApplicationRequest Server WMI Class](sms_userapplicationrequest-server-wmi-class.md)
