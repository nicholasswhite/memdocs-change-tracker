---
description: Article outlining the use of SMS_SIIB_SenderType in Configuration Manager to represent the sender type in Configuration Manager property pages.
title: "SMS_SIIB_SenderType Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_SIIB_SenderType Server WMI Class

The `SMS_SIIB_SenderType` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the sender type for the associated Configuration Manager console property pages.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SIIB_SenderType : SMS_SiteInstallItemBase
{
   String ChmFile;
   UInt32 DescriptionID;
   UInt32 DispIconID;
   UInt32 DispNameID;
   UInt32 Flags;
   String GUID;
   String HtmFile;
   String ItemName;
   String ItemType;
   String ResDLL;
   String SenderType;
   String SiteCode;
   String Units[];
};
```

## Methods

The `SMS_SIIB_SenderType` class does not define any methods.

## Properties

`ChmFile` Data type: `String`

Access type: Read-only

Qualifiers: None

Compressed .chm file containing the .htm file for the sender type.

`DescriptionID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

Resource ID of the description.

`DispIconID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

Resource ID of the display icon.

`DispNameID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

Resource ID of the display name.

`Flags` Data type: `UInt32`

Access type: Read-only

Qualifiers: [bits]

Flags defining operations supported by the sender. Possible values are:

0 ALLOW_ADD

1 ALLOW_DELETE

2 ALLOW_MODIFY

`GUID` Data type: `String`

Access type: Read-only

Qualifiers: None

GUID representing the Microsoft Management Console node for the property page.

`HtmFile` Data type: `String`

Access type: Read-only

Help file (.htm) for the sender type.

`ItemName` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

See [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md).

`ItemType` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

See [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md).

`ResDLL` Data type: `String`

Access type: Read-only

Qualifiers: None

Name of the resource DLL containing the resource strings for `DescriptionID`, `DispIconID`, and `DispNameID`.

`SenderType` Data type: `String`

Access type: Read-only

Qualifiers: None

Sender service name.

`SiteCode` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md).

`Units` Data type: `String` Array

Access type: Read-only

Qualifiers: None

See [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md).

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Hierarchy Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md)
