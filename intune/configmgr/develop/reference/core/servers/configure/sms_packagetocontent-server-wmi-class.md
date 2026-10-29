---
title: "SMS_PackageToContent Server WMI Class"
description: The SMS_PackageToContent WMI class is an SMS Provider server class, in Configuration Manager, that relates a Configuration Manager package to its content.
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

# SMS_PackageToContent Server WMI Class

The `SMS_PackageToContent` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that relates a Configuration Manager package to its content.

## Syntax

```
Class SMS_PackageToContent : SMS_BaseClass
{
      SInt32 ContentID;
      String ContentSubFolder;
      String ContentUniqueID;
      SInt32 ContentVersionInPkg;
      SInt32 MinPackageVersion;
      String PackageID;
      UInt32 PackageType;
      UInt32 SecuredTypeID;
      String SecureObjectID;
};
```

## Methods

The following table lists the methods in `SMS_PackageToContent`.

| Method | Description |
| --- | --- |
| [IsContentValid Method in Class SMS_PackageToContent](iscontentvalid-method-in-class-sms_packagetocontent.md) | Determines if the package content is valid. |

## Properties

`ContentID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key, Not_null]

The value of the `ContentID` property of the package.

`ContentSubFolder` Data type: `String`

Access type: Read/Write

Qualifiers: [Not_null]

The name of the subfolder in the package source folder that contains the files for the content.

`ContentUniqueID` Data type: `String`

Access type: Read-only

Qualifiers: [read, Not_null]

The unique ID for the content.

`ContentVersionInPkg` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [Not_null]

The version of the content in the package.

`MinPackageVersion` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [Not_null]

The minimum package version in which the content appears.

`PackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key, Not_null]

Configuration Manager-specific ID of the package.

`PackageType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [enumeration]

The type of the package. Possible values are:

| Value | Description |
| --- | --- |
| 0 | PKG_TYPE_REGULAR |
| 3 | PKG_TYPE_DRIVER |
| 4 | PKG_TYPE_TASK_SEQUENCE |
| 5 | PKG_TYPE_SWUPDATES |
| 257 | PKG_TYPE_IMAGE |
| 258 | PKG_TYPE_BOOTIMAGE |
| 259 | PKG_TYPE_OSINSTALLIMAGE |

`SecuredTypeID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

Secured type of related package.

`SecureObjectID` Data type: `String`

Access type: Read/Write

Qualifiers: None

Secure object ID. For app, it is model name. For others, it is package ID.

## Remarks

Class qualifiers for this class include:

- Secured
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  Your application can query this class to get the list of contents contained by a package or the list of packages that contain specified content.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
