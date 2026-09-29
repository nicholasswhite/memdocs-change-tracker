---
title: "AllowAccess Method in Class SMS_DeviceMethods"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn about the simplified syntax, parameters, return values, and requirement of the AllowAccess method.
ms.service: configuration-manager
---

# AllowAccess Method in Class SMS_DeviceMethods

The `AllowAccess` Windows Management Instrumentation (WMI) class method, in Configuration Manager, lets the Exchange ActiveSync device connect to Exchange.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 AllowAccess(
   UInt32 ResourceId
   String EASIdentities[]
);
```

#### Parameters

`ResourceId` Data type: `UInt32`

Qualifiers: [in]

ID of the resource.

`EASIdentities` Data type: `String` Array

Qualifiers: [in]

Array of Exchange ActiveSync identities.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## See Also

[SMS_DeviceMethods Server WMI Class](sms_devicemethods-server-wmi-class.md)
