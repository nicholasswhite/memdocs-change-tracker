---
title: "SMS_TaskSequenceReferencesInfo Server WMI Class"
description: The SMS_TaskSequenceReferencesInfo class associates a task sequence with its package.
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

# SMS_TaskSequenceReferencesInfo Server WMI Class

The `SMS_TaskSequenceReferencesInfo` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that associates a task sequence with its package.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_TaskSequenceReferencesInfo : SMS_BaseClass
{
      String PackageID;
      String ProgramName;
      String ReferenceDescription;
      String ReferenceName;
      String ReferencePackageID;
      UInt32 ReferencePackageType;
      String ReferenceProgramName;
      String ReferenceVersion;
};
```

## Methods

The `SMS_TaskSequenceReferencesInfo` class does not define any methods.

## Properties

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID of the task sequence package.

`ProgramName` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Name of the program associated with the task sequence.

`ReferenceDescription` Data type: `String`

Access type: Read/Write

Qualifiers: None

The long description of the reference package.

`ReferenceName` Data type: `String`

Access type: Read/Write

Qualifiers: None

The name of the reference package.

`ReferencePackageID` Data type: `String`

Access type: Read/Write

Qualifiers: None

ID of the reference package.

`ReferencePackageType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The type of the reference package. Possible values are:

| Value | Package type |
| --- | --- |
| 0 (0x0000) | PKG_TYPE_REGULAR |
| 3 (0x0003) | PKG_TYPE_DRIVER |
| 4 (0x0004) | PKG_TYPE_TASK_SEQUENCE |
| 5 (0x0005) | PKG_TYPE_SWUPDATES |
| 257 (0x0101) | PKG_TYPE_IMAGE |
| 258 0x0102) | PKG_TYPE_BOOTIMAGE |
| 259 (0x0101) | PKG_TYPE_OSINSTALLIMAGE |

`ReferenceProgramName` Data type: `String`

Access type: Read/Write

Qualifiers: None

Name of the reference program for the task sequence.

`ReferenceVersion` Data type: `String`

Access type: Read/Write

Qualifiers: None

The version of the reference package.

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
