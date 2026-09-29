---
description: Learn how to use the GetAssignedSite method to get the current assigned site of the client in Configuration Manager.
title: "GetAssignedSite Method in Class SMS_Client"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetAssignedSite Method in Class SMS_Client

In Configuration Manager, the `GetAssignedSite` method gets the current assigned site of the client.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 GetAssignedSite(
     String sSiteCode
);
```

#### Parameters

`sSiteCode` Data type: `String`

Qualifiers: [out]

The site code for the currently assigned site.

## Return Values

A `UInt32` data type that is 0 to indicate success or non-zero to indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[SMS_Client Client WMI Class](sms_client-client-wmi-class.md) [EvaluateMachinePolicy method in Class SMS_Client](evaluatemachinepolicy-method-in-class-sms_client.md) [RequestMachinePolicy method in Class SMS_Client](requestmachinepolicy-method-in-class-sms_client.md) [ResetPolicy method in Class SMS_Client](resetpolicy-method-in-class-sms_client.md) [SetAssignedSite method in Class SMS_Client](setassignedsite-method-in-class-sms_client.md) [SetGlobalLoggingConfiguration method in Class SMS_Client](setgloballoggingconfiguration-method-in-class-sms_client.md) [TriggerSchedule method in Class SMS_Client](triggerschedule-method-in-class-sms_client.md)
