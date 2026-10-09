---
title: "DeleteByQuery Method in Class SMS_StatusMessage"
description: In Configuration Manager, the DeleteByQuery WMI class method deletes status messages specified by a WQL query.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# DeleteByQuery Method in Class SMS_StatusMessage

The `DeleteByQuery` Windows Management Instrumentation (WMI) class method, in Configuration Manager, deletes status messages specified by a WQL query.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 DeleteByQuery(
      String WQLSelect
);
```

#### Parameters

`WQLSelect` Data type: `String`

Qualifiers: [in]

A WQL SELECT statement.

## Return Values

A `UInt32` data type that indicates the number of rows deleted.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_StatusMessage Server WMI Class](sms_statusmessage-server-wmi-class.md)
