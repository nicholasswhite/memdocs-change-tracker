---
description: Learn how to get the localized Microsoft Software License Terms content of a configuration item using GetEULA class.
title: "GetEULA Method in Class SMS_SoftwareUpdate"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetEULA Method in Class SMS_SoftwareUpdate

The `GetEULA` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the localized Microsoft Software License Terms content of a configuration item.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetEULA(
     String EULA
);
```

#### Parameters

`EULA` Data type: `String`

Qualifiers: [out]

The Microsoft Software License Terms.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

Your application should call this method only if the `EulaExists` property is set to `true` in the configuration item for the software update. This property is defined in the [SMS_ConfigurationItemBaseClass Server WMI Class](../compliance/sms_configurationitembaseclass-server-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SoftwareUpdate Server WMI Class](sms_softwareupdate-server-wmi-class.md)
