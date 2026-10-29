---
description: Learn how to use SMS_SIIB_SysResRole to represent a system role associated with a console property page resource.
title: "SMS_SIIB_SysResRole Server WMI Class"
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

# SMS_SIIB_SysResRole Server WMI Class

The `SMS_SIIB_SysResRole` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a system role associated with a Configuration Manager console property page resource.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SIIB_SysResRole : SMS_SiteInstallItemBase
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
   String RoleName;
   String SiteCode;
   String Units[];
};
```

## Methods

The `SMS_SIIB_SysResRole` class does not define any methods.

## Properties

`ChmFile` Data type: `String`

Access type: Read-only

Qualifiers: None

This property is deprecated.

`DescriptionID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

This property is deprecated.

`DispIconID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

This property is deprecated.

`DispNameID` Data type: `UInt32`

Access type: Read-only

Qualifiers: None

This property is deprecated.

`Flags` Data type: `UInt32`

Access type: Read-only

Qualifiers: [bits]

Role flags. Currently the only supported flag is ASSIGNABLE (0).

| Bit | Description |
| --- | --- |
| 0 | ASSIGNABLE |

`GUID` Data type: `String`

Access type: Read-only

Qualifiers: None

GUID representing the Microsoft Management Console node for the property page.

`HtmFile` Data type: `String`

Access type: Read-only

Qualifiers: None

This property is deprecated.

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

This property is deprecated.

`RoleName` Data type: `String`

Access type: Read-only

Qualifiers: None

Name of the role.

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

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md) [SMS_SiteInstallItemBase Server WMI Class](sms_siteinstallitembase-server-wmi-class.md)
