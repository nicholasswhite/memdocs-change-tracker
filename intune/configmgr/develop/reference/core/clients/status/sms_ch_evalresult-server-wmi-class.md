---
title: "SMS_CH_EvalResult Server WMI Class"
description: The SMS_CH_EvalResult Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that represents client evaluation results.
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

# SMS_CH_EvalResult Server WMI Class

The `SMS_CH_EvalResult` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents client evaluation results.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CH_EvalResult : SMS_BaseClass
{
    DateTime EvalTime;
    String HealthCheckDescription;
    String HealthCheckGUID;
    UInt32 ResourceID;
    UInt32 Result;
    UInt32 ResultCode;
    String ResultDetail;
    UInt32 ResultType;
};
```

## Methods

The `SMS_CH_EvalResult` class does not define any methods.

## Properties

`EvalTime` Data type: `DateTime`

Access type: Read-only

Qualifiers: [not_null, read]

Evaluation time.

`HealthCheckDescription` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Health Check description.

`HealthCheckGUID` Data type: `String`

Access type: Read-only

Qualifiers: [key, not_null, read]

Health check GUID.

`ResourceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, not_null, read]

Unique Configuration Manager-supplied ID for the resource.

`Result` Data type: `UInt32`

Access type: Read-only

Qualifiers: [not_null, read]

Evaluation result.

`ResultCode` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Result code.

`ResultDetail` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Result detail.

`ResultType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Result type.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
