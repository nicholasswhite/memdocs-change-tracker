---
title: "GetAdvertisements Method in Class SMS_Advertisement"
description: A Windows Management Instrumentation class method that gets the advertisement ID for a computer.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# GetAdvertisements Method in Class SMS_Advertisement

The `GetAdvertisements` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the advertisement id for a computer.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 GetAdvertisements(
     uint32  ResourceID,
     string  AdvertisementIDs[]
);
```

#### Parameters

`ResourceID` Data type: `UInt32`

Qualifiers: `[in]`

Unique Configuration Manager-supplied ID for the resource.

`AdvertisementIDs` Data type: `String` Array

Qualifiers: `[out]`

An array of unique auto-generated keys that Configuration Manager assigns to advertisements.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Advertisement Server WMI Class](sms_advertisement-server-wmi-class.md)
