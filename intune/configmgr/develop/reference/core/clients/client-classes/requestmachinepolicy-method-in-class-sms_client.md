---
title: "RequestMachinePolicy Method in Class SMS_Client"
description: In Configuration Manager, the RequestMachinePolicy method initiates a request for machine policy.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# RequestMachinePolicy Method in Class SMS_Client

The `RequestMachinePolicy` method, in Configuration Manager, initiates a request for machine policy.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 RequestMachinePolicy(
      UInt32 uFlags
);
```

#### Parameters

`uFlags` Data type: `UInt32`

Qualifiers: [in]

Flags identifying the policy. Possible values are:

| Value | Description |
| --- | --- |
| 0 | A machine policy retrieval cycle is initiated. |
| 1 | A machine policy validation cycle is initiated, and the server and client cyclical redundancy checks (CRCs) are compared to verify that the policies are in agreement. If the policies aren't in agreement, then a resynchronization is initiated. |

## Return Values

A `UInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMS_Client Client WMI Class](sms_client-client-wmi-class.md) [EvaluateMachinePolicy method in Class SMS_Client](evaluatemachinepolicy-method-in-class-sms_client.md) [GetAssignedSite method in Class SMS_Client](getassignedsite-method-in-class-sms_client.md) [ResetPolicy method in Class SMS_Client](resetpolicy-method-in-class-sms_client.md) [SetAssignedSite method in Class SMS_Client](setassignedsite-method-in-class-sms_client.md) [SetGlobalLoggingConfiguration method in Class SMS_Client](setgloballoggingconfiguration-method-in-class-sms_client.md) [TriggerSchedule method in Class SMS_Client](triggerschedule-method-in-class-sms_client.md)
