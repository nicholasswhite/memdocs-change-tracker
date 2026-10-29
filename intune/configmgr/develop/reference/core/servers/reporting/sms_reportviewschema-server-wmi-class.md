---
title: "SMS_ReportViewSchema Server WMI Class"
description: An SMS Provider server class that represents the views and columns available for building a report.
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

# SMS_ReportViewSchema Server WMI Class

The `SMS_ReportViewSchema` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the views and columns that are available for building a report.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ReportViewSchema : SMS_BaseClass
{
      Boolean IsStringType;
      String ViewColumnName;
      String ViewName;
};
```

## Methods

The following table shows the methods in `SMS_ReportViewSchema`.

| Method | Description |
| --- | --- |
| [GetSampleValues Method in Class SMS_ReportViewSchema](getsamplevalues-method-in-class-sms_reportviewschema.md) | Gets sample values for a report view schema. |

## Properties

`IsStringType` Data type: `Boolean`

Access type: Read Only

Qualifiers: None

`true` if the values of the column are strings.

`ViewColumnName` Data type: `String`

Access type: Read Only

Qualifiers: [key]

Name of a column in the view.

`ViewName` Data type: `String`

Access type: Read Only

Qualifiers: [key]

Name of a view.

## Remarks

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
