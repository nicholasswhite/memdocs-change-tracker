---
title: "SMS_SummarizationInterval Server WMI Class"
description: The SMS_SummarizationInterval WMI class represents the months that have been summarized by a monthly usage summary.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_SummarizationInterval Server WMI Class

The `SMS_SummarizationInterval` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the months that have been summarized by a monthly usage summary.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SummarizationInterval : SMS_BaseClass
{
      DateTime IntervalStart;
      UInt32 TimeKey;
};
```

## Methods

The `SMS_SummarizationInterval` class does not define any methods.

## Properties

`IntervalStart` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

Date and time when the software metering interval starts.

`TimeKey` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Key that uniquely identifies the interval, equivalent to 100\*Year+Month.

## Remarks

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

This class is the source for the `TimeKey` property in a monthly usage summary represented by [SMS_MonthlyUsageSummary Server WMI Class](sms_monthlyusagesummary-server-wmi-class.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MonthlyUsageSummary Server WMI Class](sms_monthlyusagesummary-server-wmi-class.md)
