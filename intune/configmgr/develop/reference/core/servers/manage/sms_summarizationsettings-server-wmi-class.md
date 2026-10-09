---
title: "SMS_SummarizationSettings Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents the site summarization settings for a site.
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

# SMS_SummarizationSettings Server WMI Class

The `SMS_SummarizationSettings` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the site summarization settings for a site.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SummarizationSettings : SMS_BaseClass
{
    String ComponentName;
};
```

## Methods

The following table lists the methods in the `SMS_SummarizationSettings` class.

| Method | Description |
| --- | --- |
| [GetSummarizationSettings Method in Class SMS_SummarizationSettings](getsummarizationsettings-method-in-class-sms_summarizationsettings.md) | Gets the summarization schedule. |
| [SetSummarizationSettings Method in Class SMS_SummarizationSettings](setsummarizationsettings-method-in-class-sms_summarizationsettings.md) | Sets the summarization schedule. |

## Properties

`ComponentName` Data type: `String`

Access type: Read

Qualifiers: [key, not_null, read]

Name of the Configuration Manager component.

## Remarks

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
