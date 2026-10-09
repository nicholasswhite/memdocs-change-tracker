---
description: Learn how to get the summarization schedule using the GetSummarizationSettings class method in Configuration Manager.
title: "GetSummarizationSettings Method in Class SMS_SummarizationSettings"
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

# GetSummarizationSettings Method in Class SMS_SummarizationSettings

The `GetSummarizationSettings` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets the summarization schedule.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
sint32 GetSummarizationSettings(
     string SiteCode,
     uint32 SummarizationType,
     uint32 FirstIntervalMins,
     uint32 SecondIntervalMins,
     uint32 ThirdIntervalMins
);
```

#### Parameters

`SiteCode` Data type: `String`

Qualifiers: [in]

The site code of the site associated with the summarization settings.

`SummarizationType` Data type: `UInt32`

Qualifiers: [in]

Types of summarization. Possible values are:

| Value | Summarization type |
| --- | --- |
| 2 | Application Deployment Summarization |
| 3 | Application State Summarization (spans all previous and current deployments) |

`FirstIntervalMins` Data type: `UInt32`

Qualifiers: [out]

The interval in minutes between summarizations for deployments that have a start date within 30 days (for deployment summarizations) or applications that have been created in the last 30 days (for application state summarization).

`SecondIntervalMins` Data type: `UInt32`

Qualifiers: [out]

The interval in minutes between summarizations for deployments that have a start date within the last 30-90 days (for deployment summarizations) or applications that have been created within the last 30-90 days (for application state summarization).

`ThirdIntervalMins` Data type: `UInt32`

Qualifiers: [out]

The interval in minutes between summarizations for deployments that have a start date over 90 days (for deployment summarizations) or applications that have been created over 90 days ago (for application state summarization).

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_SummarizationSettings Server WMI Class](sms_summarizationsettings-server-wmi-class.md)
