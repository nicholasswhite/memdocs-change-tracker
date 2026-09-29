---
title: "SyncToken Method in Class SMS_MDMAppleVppToken"
description: Initiate a synchronization of the Apple Volume Purchase Program (VPP) token.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# SyncToken Method in Class SMS_MDMAppleVppToken

The `SyncToken` Windows Management Instrumentation (WMI) class method, in Configuration Manager, initiates a synchronization of the Apple Volume Purchase Program (VPP) token.

## Syntax

```
sint32 SyncToken(
     String TokenID
);

```

#### Parameters

`TokenID` Data type: `String`

Qualifiers: [in]

The ID of the Apple VPP token.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MDMAppleVppToken Server WMI Class](sms_mdmapplevpptoken-server-wmi-class.md)
