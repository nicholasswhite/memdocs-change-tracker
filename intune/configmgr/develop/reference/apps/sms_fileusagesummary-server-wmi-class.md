---
title: "SMS_FileUsageSummary Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: Learn about the simplified syntax, methods, properties and requirements of the SMS_FileUsageSummary server class.
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

# SMS_FileUsageSummary Server WMI Class

The `SMS_FileUsageSummary` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides a usage summary of a metered file.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_FileUsageSummary : SMS_BaseClass
{
      UInt32 DistinctUserCount;
      SInt64 FileID;
      DateTime IntervalStart;
      UInt32 IntervalWidth;
      String SiteCode;
};
```

## Methods

The `SMS_FileUsageSummary` class does not define any methods.

## Properties

`DistinctUserCount` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Count of the distinct number of users who used the file during the summarization interval.

`FileID` Data type: `SInt64`

Access type: Read/Write

Qualifiers: [key]

File ID of the summarized file. To find the file information, match `FileID` with the ID in [SMS_ProductFileInfo Server WMI Class](sms_productfileinfo-server-wmi-class.md). To find the rules that caused the file to be metered, match `FileID` to the ID in [SMS_MeteredFiles Server WMI Class](sms_meteredfiles-server-wmi-class.md).

`IntervalStart` Data type: `DateTime`

Access type: Read/Write

Qualifiers: [key]

Start time of the summarization interval.

`IntervalWidth` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

Size of the summarization interval, in minutes. Possible values are 15 and 60.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Site code for the clients that used the file during the summarization interval. This identifies the site that originally generated the summary.

## Remarks

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

This class counts the number of distinct users and computers that used a metered file during a particular interval on a particular site.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
