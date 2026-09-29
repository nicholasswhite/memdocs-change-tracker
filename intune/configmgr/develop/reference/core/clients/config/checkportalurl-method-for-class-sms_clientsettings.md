---
description: Learn how to check if the default application catalog website point in the client agent settings is set to portalUrl.
title: "CheckPortalUrl Method for Class SMS_ClientSettings"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CheckPortalUrl Method for Class SMS_ClientSettings

The `CheckPortalUrl` Windows Management Instrumentation (WMI) class method, in Configuration Manager, checks whether the default application catalog website point in the default or custom client agent settings is set to `portalUrl`.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 CheckPortalUrl(
     string PortalUrl,
     boolean isUsed
);
```

#### Parameters

`PortalUrl` Data type: `String`

Qualifiers: `[in]`

PortalUrl.

`isUsed` Data type: `Boolean`

Qualifiers: `[out]`

isUsed.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ClientSettings Server WMI Class](sms_clientsettings-server-wmi-class.md)
