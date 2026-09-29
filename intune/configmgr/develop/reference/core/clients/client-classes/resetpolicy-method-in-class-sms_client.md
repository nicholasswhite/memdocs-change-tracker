---
description: Learn how to reset the policy on a client resulting in the next policy request receiving a full policy in Configuration Manager.
title: "ResetPolicy Method in Class SMS_Client"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ResetPolicy Method in Class SMS_Client

In Configuration Manager, the `ResetPolicy` method, resets the policy on a client. As a result, the next policy request will receive a full policy instead of merely the change in policy since the last policy request.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 ResetPolicy(
     UInt32 uFlags
);
```

#### Parameters

`uFlags` Data type: `UInt32`

Qualifiers: [in]

Flags identifying the policy. Possible values are:

| Value | Description |
| --- | --- |
| 0 | The next policy request will be for a full policy instead of the change in policy since the last policy request. |
| 1 | The existing policy will be purged completely. |

## Return Values

A `UInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Remarks

Indiscriminate calling of this method could have adverse effects. For example, if you purge the existing policy (`ulFlags` = 1) software distribution programs could be run more than once. If the request is for full policy (`ulFlags` = 0), you could generate unnecessary network traffic.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMS_Client Client WMI Class](sms_client-client-wmi-class.md) [EvaluateMachinePolicy method in Class SMS_Client](evaluatemachinepolicy-method-in-class-sms_client.md) [GetAssignedSite method in Class SMS_Client](getassignedsite-method-in-class-sms_client.md) [RequestMachinePolicy method in Class SMS_Client](requestmachinepolicy-method-in-class-sms_client.md) [SetAssignedSite method in Class SMS_Client](setassignedsite-method-in-class-sms_client.md) [SetGlobalLoggingConfiguration method in Class SMS_Client](setgloballoggingconfiguration-method-in-class-sms_client.md) [TriggerSchedule method in Class SMS_Client](triggerschedule-method-in-class-sms_client.md)
