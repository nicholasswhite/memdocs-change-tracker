---
title: "SMS_SummarizationSettings Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents the site summarization settings for a site.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
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
