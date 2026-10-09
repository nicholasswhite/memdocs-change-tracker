---
description: Learn how to get sample values for a report view schema using GetSampleValues class method Configuration Manager.
title: "GetSampleValues Method in Class SMS_ReportViewSchema"
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

# GetSampleValues Method in Class SMS_ReportViewSchema

The `GetSampleValues` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets sample values for a report view schema.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 GetSampleValues(
   UInt32 RangeBegin,
   UInt32 RangeEnd,
   String Filter,
   UInt32 TotalValuesAvailable,
   String Values[]
);
```

#### Parameters

`RangeBegin` Data type: `UInt32`

Qualifiers: [in]

Value indicating the beginning of the range of sample values.

`RangeEnd` Data type: `UInt32`

Qualifiers: [in]

Value indicating the end of the range of sample values.

`Filter` Data type: `String`

Qualifiers: [in]

Filter to use for retrieval of sample values.

`TotalValuesAvailable` Data type: `UInt32`

Qualifiers: [out]

The number of sample values retrieved in the `Values` parameter.

`Values` Data type: `String` Array

Qualifiers: [out]

The retrieved sample values.

## Return Values

A `UInt32` data type.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ReportViewSchema Server WMI Class](sms_reportviewschema-server-wmi-class.md)
