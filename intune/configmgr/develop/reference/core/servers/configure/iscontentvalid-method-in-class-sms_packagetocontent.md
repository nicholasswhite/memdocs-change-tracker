---
description: Learn how to determine if the package content is valid using IsContentValid WMI class method in Configuration Manager.
title: "IsContentValid Method in Class SMS_PackageToContent"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# IsContentValid Method in Class SMS_PackageToContent

The `IsContentValid` Windows Management (WMI) class method, in Configuration Manager, determines if the package content is valid.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
Boolean IsContentValid();
```

#### Parameters

None.

## Return Values

A `Boolean` data type that is `true` if the package contains all the files for the content; otherwise `false`.

## Remarks

This method checks the package to ensure that all files are available for the content. It also checks to ensure that the licensing terms are met.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_PackageToContent Server WMI Class](sms_packagetocontent-server-wmi-class.md)
