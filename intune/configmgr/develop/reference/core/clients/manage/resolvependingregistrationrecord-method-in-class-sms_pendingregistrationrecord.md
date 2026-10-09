---
title: "ResolvePendingRegistrationRecord Method in Class SMS_PendingRegistrationRecord"
description: The ResolvePendingRegistrationRecord Windows Management Instrumentation (WMI) class method resolves any conflicts for the pending registration records.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
---

# ResolvePendingRegistrationRecord Method in Class SMS_PendingRegistrationRecord

The `ResolvePendingRegistrationRecord` Windows Management Instrumentation (WMI) class method, in Configuration Manager, resolves any conflicts for the pending registration records.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 ResolvePendingRegistrationRecord(
     string SMSID,
     uint32 Action
);
```

#### Parameters

`SMSID` Data type: `String`

Qualifiers: [in]

Pending registration record id to use.

`Action` Data type: `UInt32`

Qualifiers: [in]

Action to execute on the pending registration record. Possible values are:

| Value | Description |
| --- | --- |
| 1 | Merge: Allows the record to take over the existing conflicting record. |
| 2 | New: Creates a new record for the `SMSID` resource. This resource is then issued a new `SMSID` value. |
| 3 | Reject: Creates a new record for the `SMSID` resource. This resource is then issued a new `SMSID` value, but is restricted from communicating with the Configuration Manager site. |

## Return Values

An `SInt32`data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Site Server WMI Class](../../servers/configure/sms_site-server-wmi-class.md)
