---
title: "SMS_WinPEOptionalComponentInBootImage Server WMI Class"
description: This is an SMS Provider server class in Configuration Manager. It represents the association between a boot image package and a WinPE optional component.
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

# SMS_WinPEOptionalComponentInBootImage Server WMI Class

The `SMS_WinPEOptionalComponentInBootImage` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents the association between a boot image package and a WinPE optional component.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_WinPEOptionalComponentInBootImage : SMS_BaseClass
{
    String Architecture;
    UInt32 ComponentID;
    String DependentComponentNames[];
    UInt32 DependentIds[];
    Boolean IsRequired;
    String Name;
    String PackageID;
    UInt64 Size;
};
```

## Methods

The `SMS_WinPEOptionalComponentInBootImage` class does not define any methods.

## Properties

`Architecture` Data type: `String`

Access type: Read

Qualifiers: [key]

The architecture of WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

`ComponentID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The unique identifier of the WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

`DependentComponentNames` Data type: `String` Array

Access type: Read

Qualifiers: none

The name of dependent WinPE optional components associated with the SMS_WinPEOptionalComponentInfo object.

`DependentIds` Data type: `UInt32` Array

Access type: Read

Qualifiers: none

The unique identifier of dependent WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

`IsRequired` Data type: `Boolean`

Access type: Read

Qualifiers: none

The required flag of WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

`Name` Data type: `String`

Access type: Read

Qualifiers: none

The name of WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

`PackageID` Data type: `String`

Access type: Read

Qualifiers: [key]

The unique identifier of the boot image associated with the SMS_BootImagePackage object.

`Size` Data type: `UInt64`

Access type: Read

Qualifiers: none

The size of WinPE optional component associated with the SMS_WinPEOptionalComponentInfo object.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
