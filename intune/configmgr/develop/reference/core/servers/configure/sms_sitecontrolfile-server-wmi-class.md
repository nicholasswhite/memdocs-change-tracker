---
description: Learn how to use the SMS_SiteControlFile class which represents the site control file and methods to maintain version control of the site control file.
title: "SMS_SiteControlFile Server WMI Class"
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

# SMS_SiteControlFile Server WMI Class

The `SMS_SiteControlFile` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the site control file and contains methods to maintain version control of the site control file.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SiteControlFile : SMS_BaseClass
{
     String BuildNumber;
     UInt32 FileType;
     String FormatVersion;
     String SCFData;
     UInt32 SerialNumber;
     String SiteCode;
};
```

## Methods

The `SMS_SiteControlFile` class does not define any methods.

## Properties

`BuildNumber` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

Build number of the Configuration Manager installation that creates the site control file. The default value is "".

`FileType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key, enumeration:ToSubClass]

This property is deprecated.

`FormatVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

Version of the site control file format. The default value is "".

`SCFData` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy, large]

Current site control file data in text format (accumulated deltas).

`SerialNumber` Data type: `UInt32`

Access type: ReadWrite

Qualifiers: [key]

Unique ID of the file itself. The number is incremented every time the file changes. The default value is 0.

`SiteCode` Data type: `String`

Access type: Read-only

Qualifiers: [key, read, SizeLimit("3")]

Site code of the site associated with the site control file. The default value is "".

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  Your application uses the methods of this class to perform version control of the site control file. To update the contents of the site control file, the application should use classes derived from [SMS_SiteControlItem Server WMI Class](sms_sitecontrolitem-server-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SiteControlItem Server WMI Class](sms_sitecontrolitem-server-wmi-class.md)
