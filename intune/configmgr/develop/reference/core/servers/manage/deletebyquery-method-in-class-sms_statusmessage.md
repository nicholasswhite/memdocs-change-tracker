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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
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
