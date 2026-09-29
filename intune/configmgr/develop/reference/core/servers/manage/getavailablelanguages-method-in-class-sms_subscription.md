---
description: Learn how to use the GetAvailableLanguages method on the SMS_Subscription class to obtain a list of available languages.
title: "GetAvailableLanguages Method in Class SMS_Subscription"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetAvailableLanguages Method in Class SMS_Subscription

The `GetAvailableLanguages` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the available languages.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 GetAvailableLanguages(
     UInt32 LocaleIDs[]
);
```

#### Parameters

`LocaleIDs` Data type: `UInt32` array

Qualifiers: `[out]`

The identifiers of the locales associated with the localized information.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See also

[SMS_Alert server WMI class](sms_alert-server-wmi-class.md)
